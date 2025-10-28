# Installation
1. [Installation guidance](https://reactionmechanismgenerator.github.io/RMG-Py/users/rmg/installation/index.html)
	1. Download and install "Docker"
	2. In terminal "docker pull reactionmechanismgenerator/rmg:3.3.0"
	3. docker run --name rmgcontainer -v "/Users/kims910/_PNNL_SKim/Research/myrmgfiles" -it reactionmechanismgenerator/rmg:3.3.0
	4. to leave: "exit" or enter again "docker start rmgcontainer --attach --interactive"
2. [First RMG job](https://www.youtube.com/watch?v=_YjUFG3uB0s)
	1. "python rmg.py --help"
	2. "python /rmg/RMG-Py/rmg.py examples/rmg/superminimal/input.py"
	3. [Example of input file](https://reactionmechanismgenerator.github.io/RMG-Py/users/rmg/examples.html)
	4. 