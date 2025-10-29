# Installation 2025 # 2
1. [Installation guidance #2](https://reactionmechanismgenerator.github.io/RMG-Py/users/rmg/installation/index.html)
	1. Download and install "Docker"
	2. In terminal "docker pull reactionmechanismgenerator/rmg:3.3.0"
	3. docker scout quickview reactionmechanismgenerator/rmg:3.2.0
	4. docker run --name rmgcontainer -v "/Users/kims910/_PNNL_SKim/Research/myrmgfiles:/rmg/RMG-Py/myrmgfiles" -it reactionmechanismgenerator/rmg:3.3.0
	5. For with jupyter
	   docker run --name rmgcontainer -p 8888:8888 -v "/Users/kims910/_PNNL_SKim/Research/myrmgfiles:/rmg/RMG-Py/myrmgfiles" -it reactionmechanismgenerator/rmg:3.3.0
	6. to leave: "exit" or enter again "docker start rmgcontainer --attach --interactive"

# First RMG job # 3
1. [First RMG job #3](https://www.youtube.com/watch?v=_YjUFG3uB0s)
	1. Vscode
		1. Installing a extension 
			1. Docker
			2. dev container
			3. Container tools
		2. Remote explorer and run rmg container
		3. open a new terminal and explorer the folders
	2. "python rmg.py --help"
	3. "python /rmg/RMG-Py/rmg.py /rmg/RMG-Py/examples/rmg/superminimal/input.py"
	4. [Example of input file](https://reactionmechanismgenerator.github.io/RMG-Py/users/rmg/examples.html)
 
# Molecular representation # 4 
1. Jupyter
	1. [Take a look from 2023 seminar #13 Simulation and sensitivity analysis](https://www.youtube.com/watch?v=H6AB4CB-59Q&t=360s) or [#8](https://www.youtube.com/watch?v=H6AB4CB-59Q&t=360s)
	2. docker container rm rmgcontainer
	3. docker run --name rmgcontainer -p 8888:8888 -v "/Users/kims910/_PNNL_SKim/Research/myrmgfiles:/rmg/RMG-Py/myrmgfiles" -it reactionmechanismgenerator/rmg:3.3.0
	4. docker start rmgcontainer -ai
	5. cd /rmg; jupyter notebook --allow-root --ip 0.0.0.0 --no-browser
	6. browser: [localhost:8888](http://localhost:8888) —>copy the token from the terminal and then paste token
2. [Molecular representation #4](https://www.youtube.com/watch?v=5mTwqKcWAhI)
	1. [Molecular search in rmg](https://rmg.mit.edu/molecule_search) 
	2. Useful tools
		1. [molecule search](https://rmg.mit.edu/molecule_search)
		2. [Draw functional groups](https://rmg.mit.edu/tools/group_draw)
	3. In Jupyter 
		1. from rmgpy.molecule import Molecule 
		2. m = Molecule(smiles="CC")
		3. display(m)
		4. str(m) ; 
		   '<Molecule "CC">'
		5. print(m.to_adjacency_list());
		   1 C u0 p0 c0 {2,S} {3,S} {4,S} {5,S}
		   2 C u0 p0 c0 {1,S} {6,S} {7,S} {8,S}
		   3 H u0 p0 c0 {1,S}
		   4 H u0 p0 c0 {1,S}
		   5 H u0 p0 c0 {1,S}
		   6 H u0 p0 c0 {2,S}
		   7 H u0 p0 c0 {2,S}
		   8 H u0 p0 c0 {2,S}
		   
		6. m = Molecule(smiles="CCcC=CC")
		7. m.generate_resonance_structures
		8. for i in m.generate_resonance_structures():
		   display (i)

# Running RMG jobs # 5
1. General procedure for running 
	1. python /rmg/RMG-Py/rmg.py *option* */path/to/your/input.py*
		1. 
