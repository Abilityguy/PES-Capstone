# Capstone Project

## Car Parking Environment
* Install Unity (2020 or higher versions)
* Clone the repository - https://github.com/dilmerv/UnityMLEssentials
* Replace the ‘Assets/Scripts’ folder with the code submission provided.
* Install the Unity ML-Agents toolkit from https://github.com/Unity-Technologies/ml-agents
* Open the Car Parking project in Unity. (Path: UnityMLEssentials/Assets/Scenes/ParkingLot.unity)
* Under the Agent tab, you can select between training or inference mode for the model.
* Press the play button.

## MiniGrip Environment
* Unzip MiniGrid_scripts.zip
* To train a model on a particular environment run 
  

  OMP_NUM_THREADS=1 python -m monobeast.minigrid.monobeast_amigo --env $Env_Name --num_actors $num_actors --modify --generator_batch_size $generator_batch_size --generator_learning_rate $generator_learning_rate  --generator_entropy_cost $generator_entropy_cost --alpha $alpha --savedir $save_path --load_module $load_path


  Example :-


  OMP_NUM_THREADS=1 python -m monobeast.minigrid.monobeast_amigo --env MiniGrid-LavaCrossingS9N3-v0 --num_actors 40 --modify --generator_batch_size 150 --generator_learning_rate 0.001 --generator_reward_negative -.3 --generator_entropy_cost .01 --alpha 0.7 --savedir ./lavaS9N3 --xpid 201 --load_module ./lavaS9N3/201/model.tar 


* To test the model on a particular environment run

	
	OMP_NUM_THREADS=1 python -m monobeast.minigrid.monobeast_amigo --env $Env_name --num_actors 1 --modify --generator_batch_size $generator_batch_size --generator_learning_rate $generator_learning_rate  --generator_entropy_cost $generator_entropy_cost --alpha $alpha --load_module $load_path


	Example :-


	OMP_NUM_THREADS=1 python -m monobeast.minigrid.monobeast_amigo --env MiniGrid-DoorKey-8x8-v0 --num_actors 1 --modify --generator_batch_size 150 --generator_entropy_cost .05 --generator_reward_negative -.3 --savedir ./8x8 --xpid 20 --total_frames 10000000000 --load_module ./8x8/model.tar