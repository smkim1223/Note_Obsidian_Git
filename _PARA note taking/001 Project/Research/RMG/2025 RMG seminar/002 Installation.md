# Installation 2025 # 2
1. [Installation guidance #2](https://reactionmechanismgenerator.github.io/RMG-Py/users/rmg/installation/index.html)
	1. Download and install "Docker"
	2. In terminal "docker pull reactionmechanismgenerator/rmg:3.3.0"
	3. docker scout quickview reactionmechanismgenerator/rmg:3.2.0
	4. docker run --name rmgcontainer -v "/Users/kims910/_PNNL_SKim/Research/myrmgfiles:/rmg/RMG-Py/myrmgfiles" -it reactionmechanismgenerator/rmg:3.3.0
	5. For with jupyter
	   docker run --name rmgcontainer -p 8888:8888 -v "/Users/kims910/_PNNL_SKim/Research/myrmgfiles:/rmg/RMG-Py/myrmgfiles" -it reactionmechanismgenerator/rmg:3.3.0
	6. to leave: "exit" or enter again "docker start rmgcontainer --attach --interactive"