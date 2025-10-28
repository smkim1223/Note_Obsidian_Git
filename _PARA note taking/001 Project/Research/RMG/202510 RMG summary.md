# Installation
1. [Installation guidance](https://reactionmechanismgenerator.github.io/RMG-Py/users/rmg/installation/index.html)
	1. Download and install "Docker"
	2. In terminal "docker pull reactionmechanismgenerator/rmg:3.3.0"
	3. docker scout quickview reactionmechanismgenerator/rmg:3.2.0
	4. docker run --name rmgcontainer -v "/Users/kims910/_PNNL_SKim/Research/myrmgfiles:/rmg/RMG-Py/myrmgfiles" -it reactionmechanismgenerator/rmg:3.3.0
	5. For with jupyter
	   docker run --name rmgcontainer -p 8888:8888 -v "/Users/kims910/_PNNL_SKim/Research/myrmgfiles:/rmg/RMG-Py/myrmgfiles" -it reactionmechanismgenerator/rmg:3.3.0
	6. to leave: "exit" or enter again "docker start rmgcontainer --attach --interactive"
2. [First RMG job](https://www.youtube.com/watch?v=_YjUFG3uB0s)
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
3. Jupyter 
	1. docker container rm rmgcontainer
	2. docker run --name rmgcontainer -p 8888:8888 -v "/Users/kims910/_PNNL_SKim/Research/myrmgfiles:/rmg/RMG-Py/myrmgfiles" -it reactionmechanismgenerator/rmg:3.3.0
	3. docker start rmgcontainer -ai
	4. cd /rmg; jupyter notebook --allow-root --ip 0.0.0.0 --no-browser
4. browser: [localhost:8888](http://localhost:8888) —>copy the token from the terminal and then paste token