# Capstone Project

## Car Parking Environment
* Install Unity (2020 or higher versions)
* Clone the repository - https://github.com/dilmerv/UnityMLEssentials
* Replace the ‘Assets/Scripts’ folder with the code submission provided.
* Install the Unity ML-Agents toolkit from https://github.com/Unity-Technologies/ml-agents
* Open the Car Parking project in Unity. (Path: UnityMLEssentials/Assets/Scenes/ParkingLot.unity)
* Under the Agent tab, you can select between training or inference mode for the model.
* Press the play button.

## MiniGrid Environment
* Unzip MiniGrid_scripts.zip
* pip install -r requirements.txt
* To train a model on a particular environment run 
  

  OMP_NUM_THREADS=1 python -m monobeast.minigrid.monobeast_amigo --env $Env_Name --num_actors $num_actors --modify --generator_batch_size $generator_batch_size --generator_learning_rate $generator_learning_rate  --generator_entropy_cost $generator_entropy_cost --alpha $alpha --savedir $save_path --load_module $load_path


  Example :-


  OMP_NUM_THREADS=1 python -m monobeast.minigrid.monobeast_amigo --env MiniGrid-LavaCrossingS9N3-v0 --num_actors 40 --modify --generator_batch_size 150 --generator_learning_rate 0.001 --generator_reward_negative -.3 --generator_entropy_cost .01 --alpha 0.7 --savedir ./lavaS9N3 --xpid 201 --load_module ./lavaS9N3/201/model.tar 


* To test the model on a particular environment run

	
	OMP_NUM_THREADS=1 python -m monobeast.minigrid.monobeast_amigo --env $Env_name --num_actors 1 --modify --generator_batch_size $generator_batch_size --generator_learning_rate $generator_learning_rate  --generator_entropy_cost $generator_entropy_cost --alpha $alpha --load_module $load_path


	Example :-


	OMP_NUM_THREADS=1 python -m monobeast.minigrid.monobeast_amigo --env MiniGrid-DoorKey-8x8-v0 --num_actors 1 --modify --generator_batch_size 150 --generator_entropy_cost .05 --generator_reward_negative -.3 --savedir ./8x8 --xpid 20 --total_frames 10000000000 --load_module ./8x8/model.tar
	
## RoboND Rover
* Run Roversim.x86_64 to start the simulator. 
* Choose the appropriate graphics settings and start the simulator.
* Choose Autonomous mode option in the simulator.
* Run the driver python file at code/drive_rover.py
* The driver creates a socket and waits for the simulator to connect. Then, it starts the process of mapping the environment and collecting the goals.

## Genetic Algorithm Scripts
* Clone [this](https://github.com/rgarzonj/gym-blocksworld) repository.
* Download the bwstates sources from ftp://arp.anu.edu.au/pub/bwstates.1.tar.gz
* Untar and unzip the file with tar xvfz bwstates.1.tar.gz (this will create a folder bwstates.1)
* Copy the entire folder bwstates.1 into the folder /gym-blocksworld/gym_blocksworld/envs/BWSTATES
* Compile the sources in the folder bwstates.1 (follow the instructions in bwstates1/README.ms). This should generate a binary file /bwstates.1/bwstates
* Go to the folder containing the cloned repository (this folder should contain the cloned folder gym-blocksworld) and run the following command: `pip install -e gym-blocksworld`
* Run the command python3 genetic_algo/genetic_algo_deap.py
