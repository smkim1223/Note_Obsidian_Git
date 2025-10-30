Running RMG jobs # 5
1. General procedure for running 
	1. [Presentation](https://www.youtube.com/watch?v=-K6fLPgVkWc)
	2. python /rmg/RMG-Py/rmg.py *option* */path/to/your/input.py*
		1. Full list of optional argument: -h or --help 
		2. To specify maximum run time: -t or --walltime
		3. to run in parallel: -n or --maxproc
	3. RMG input files
		1. RMG-Py/examples/rmg 
		2. [Gitub](https://github.com/ReactionMechanismGenerator/RMG-Py) or [RMG documentation](https://reactionmechanismgenerator.github.io/RMG-Py/users/rmg/input.html) 
		3. RMG input files consisted of database / species / reactors / model


This note summarizes the essential information regarding environment setup, input file construction, and diagnostics for running Reaction Mechanism Generator (RMG) jobs, structured for a comprehensive hands-on session.

## 1. Execution, Environment, and Resources

### A. General Syntax and Paths

The general command structure for running RMG is to provide `python`, the path to the `rmg.py` script, any extra options, and the path to your input file. Giving the **correct paths** is a very important concept.

- **Path Configuration:** To avoid typing the long path to `rmg.py` repeatedly, you can add the path environment variable line to your `.bashrc` file or run it once.
- **Output Location:** By default, all output files are generated in the same directory as your input file.

### B. Environment Activation

If you are using the developer version (and not Docker), you must ensure the correct Conda environment is active by running: `conda activate rmg_env`. The terminal prompt should show `(rmg_env)`, not `(base)`.

### C. Extra Arguments

Useful optional arguments to include in your run command:

- **`-h`**: Lists all available help options for `rmg.py`.
- **`-T`**: Specifies the **wall time** (the maximum run time allowed for RMG). This is helpful for ensuring consistency when comparing different runs or libraries, but ensure the time is not cut too short, which could cause a truncation error.
- **`-n`**: A parallelization option for specifying the number of processors. Note that RMG has limitations on the extent of parallel processing it can utilize.

### D. Key Resources

RMG is a huge software package. It is strongly recommended to check the **documentation** and the **RMG website** (GitHub page) frequently, as they contain critical information.

## 2. RMG Input File Structure

The input file consists of blocks defining the databases, species, reactors, and model parameters.

### A. Database Specifications

These blocks tell RMG which reference data to use. If RMG needs a value, it checks libraries first (as they are usually higher accuracy) before resorting to estimation.

|Parameter|Function and Notes|Citations|
|:--|:--|:--|
|`thermoLibraries`|Lists highly accurate libraries for thermodynamics estimation. **Priority is key:** RMG uses the value from the **first library** where a species is found; therefore, list the most accurate libraries first.||
|`reactionLibraries`|Lists kinetics libraries. These reactions are automatically added to the **edge**.||
|`seedMechanisms`|Sets of reactions that are automatically added into the model **core**. **Consistency:** Use thermo libraries that match the kinetics specified in the seed mechanism (e.g., Klippenstein's thermo for Klippenstein's seed) because reaction rates are often dependent on the corresponding thermochemistry.||
|`kineticsFamilies`|Templates defining how RMG can generate reactions (e.g., H-abstraction, disproportionation). `default` is usually sufficient for gas mechanisms.||
|`kineticsEstimator`|`rate rules` is currently the only available option for estimating kinetics. Estimation happens automatically if a rate is not found in a listed library.||

### B. Species Descriptions

- Listing a species in the input file automatically adds it to the model **core**. This is recommended to help make models consistent across runs by ensuring core species are created in the same order and share the same name.
- Species can be described using InChI, SMILES, or an adjacency list.
- Use `reactive=False` to designate a species (e.g., nitrogen) that RMG will not attempt to generate reactions for, treating it as a bath gas.

### C. Reactors and Termination Criteria

You must specify **at least one reactor**.

- **`simpleReactor`**: Typically models a batch reactor with constant pressure (P) and temperature (T). Required inputs are T, P, and initial mole fractions.
- **`ranged reactors`**: Used to sample a multidimensional grid of T, P, and composition conditions. RMG generates a **single network** that operates correctly across all specified grid points.
- **Specialty Reactors**: RMG supports `liquid reactor` (requires specifying solvent) and `surface reactors` (requires specifying `catalystProperties` and initial surface coverages).

#### Termination Criteria

At least one criterion must be specified; they act as "this condition **or** the other condition".

1. `terminationConversion`: Ends the simulation when a specified percentage of a reactant is consumed (e.g., 99% conversion).
2. `terminationTime`: Ends the simulation after a set duration.
3. `terminationRateRatio`: Ends when the active chemistry reaches a steady state, determined by the ratio of current flux to the most active characteristic flux observed.

### D. Model and Simulation Parameters (Tolerances)

These parameters control the RMG algorithm based on characteristic flux. Tolerances are relative to the characteristic flux, not absolute values.

|Parameter|Purpose/Function|Typical Value/Action|Citations|
|:--|:--|:--|:--|
|`toleranceMoveToCore`|Threshold flux (relative to the characteristic flux) required for a species to be moved from the edge to the core.|Default is usually **0.1** (10%).||
|`toleranceKeepInEdge`|Used for **pruning**. Species whose flux stays below this level may be pruned from the edge. Decreasing this tolerance will result in a larger model.||
|`toleranceInterruptSimulation`|If flux exceeds this, the simulation stops immediately to add the new species. If pruning is active, this should be set arbitrarily high (e.g., `1e8`) to ensure the simulation finishes before pruning is evaluated.||

### E. Advanced and Miscellaneous Blocks

- **`pressureDependence`**: This block is required if you need RMG to generate pressure-dependent rates (e.g., third body fall off reactions). `modified strong collision` is the recommended method, typically parameterized by `Chebyshev` or `PLOG` rates.
- **`speciesConstraints`**: Limits the size and type of molecules RMG automatically generates (e.g., maximum carbon atoms, maximum number of radicals, maximum surface sites).
    - **Caveat:** If an input species or library species violates these constraints, you must include an explicit `allowed` section for those species, or RMG will crash.
- **Output Control (Flags that slow down the run):**
    - `generateSeedEachIteration`: Saves a copy of all species in the core and edge at every iteration, useful for restarting a crashed run.
    - `generateOutputHTML`: Saves a clickable HTML summary report, which is a very slow option.
    - `saveEdgeSpecies`: Saves copies of all species in the edge at every iteration, which is considered the slowest option because the edge can become very large.

## 3. Output Files and Diagnostics

RMG generates several files critical for analysis and debugging.

|Output File|Content/Purpose|Importance/Usage|Citations|
|:--|:--|:--|:--|
|`RMG.log`|Primary log file. Tracks RMG's progress, including species creation and final model size.|Essential diagnostic tool.||
|`chem_annotated.inp`|The generated mechanism in **CHEMKIN format**. Contains elements, species, NASA polynomials, and reaction rates (Arrhenius parameters).|Standard mechanism output.||
|`species_dictionary.txt`|Provides the precise **adjacency list definition** for every species in the model.|**Very important** for advanced analysis, debugging, and ensuring consistency when comparing mechanisms ("apples to apples").||
|Cantera `.yaml` file|The mechanism in **Cantera format**.|Only generated if the RMG run finishes to completion.||
|Transport Data File|Located in the CHEMKIN folder. Contains transport data necessary for simulations where transport is important (e.g., flame speeds).||
