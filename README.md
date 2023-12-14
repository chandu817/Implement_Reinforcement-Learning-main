# Implement_Reinforcement-Learning-main
The goal of this project is to use gaming to implement reinforcement learning.
As we develop this AI model, we plan to create a reinforcement learning model that will allow it to play Mario and see back and forth.

We're going to use Python to do this. Open AI Gym will be utilized by us.AI may be easily trained to play games and interact with various simulated environments using this common architecture. Consider Alphabetix, but on a smaller scale. For our objective, we are use the "https://pypi.org/project/gym-super-mario-bros/" environment, which is a modified version of the NES emulator running on Python.

We have written our code with explanation for every line. The "Reward function" that is used in the gym is how the environment operates.-super mario bros

Preprocessing the Environment: Since our AI will be using visuals from the Mario game to learn, we must first preprocess the data from the game before starting our AI fight. We did this by using two preprocessing steps: grayscale and frame stacking. By converting a color image to grayscale, we may reduce the amount of data our AI needs to learn. By stacking consecutive frames, we can effectively give our AI model memory, allowing it to recognize Mario and his adversaries' motions over time.

Install RL libraries: You need to have some sort GPU acceleration running either CUDA or ROCm 4.2(beta) to display your output. One can check GPU versions and install from https://pytorch.org/get-started/locally/ which ever version suits your GPU

Install Stable-Baselines3: There are certain algorithms that are available we can check it "https://stable-baselines3.readthedocs.io/en/master/" here we are going to use DQN. We used all these in wrappers that are explained in code.

Applying Vectorization: we are going to stack our frame using VecFrameStack(env, 4, channels_order='last')

Training Reinforcement model:The Proximal Policy Optimization algorithm will be employed. Initially, we will import those dependencies. After that, we will have some sample code that will let you save models while you train them. This will enable you to go back and view the various models you have created. Let's proceed and import our dependencies.

#Import os for file path management :
import os 

#Import PPO for algos :
from stable_baselines3 import PPO

#Import Base Callback for saving models :
from stable_baselines3.common.callbacks import BaseCallback
In the code we have class TrainAndLoggingCallback(BaseCallback) where you can find cod eto tain our model.

Finally Testing:
First, we will test our model by loading it from memory. However, if we were to stop training or close this notebook, we would like to be able to reload the model from a file instead of depending solely on the one we currently have in memory. To achieve this, we can use the model.load or ppo.load method.
Code says that we will train our model and then apply the learned model to the code as stated.

Lastly, the output of our code, when it runs, will open in a new window as seen in the image below.

<img width="286" alt="image" src="https://user-images.githubusercontent.com/42296536/207493951-19138e15-5b97-459c-ba4d-45431bf337dc.png">

