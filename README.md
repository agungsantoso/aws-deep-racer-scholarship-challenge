# AWS DeepRacer Scholarship Challenge 2019 Notes


![GitHub](https://img.shields.io/github/license/mashape/apistatus.svg)

<p align="center">
  <img src="./assets/badge.png" width="25%">
</p>

A collection of notes on AWS DeepRacer Scholarship Challenge 2019.

Contributions are always welcome!

<!-- toc -->

- [Lesson 1: Welcome! Important Details on the AWS DeepRacer Scholarship](#lesson-1-welcome-important-details-on-the-aws-deepracer-scholarship)
  * [1. AWS DeepRacer Scholarship Challenge](#1-aws-deepracer-scholarship-challenge)
- [Lesson 2: Get Started with AWS DeepRacer](#lesson-2-get-started-with-aws-deepracer)
  * [1. Intro to AWS DeepRacer](#1-intro-to-aws-deepracer)
  * [2. Welcome](#2-welcome)
  * [3. RL in AWS DeepRacer](#3-rl-in-aws-deepracer)
  * [4. Unboxing AWS DeepRacer](#4-unboxing-aws-deepracer)
  * [5. Under the Hood](#5-under-the-hood)
  * [6. DeepRacer Assembly](#6-deepracer-assembly)
  * [7. Steering Calibration](#7-steering-calibration)
  * [8. Throttle Calibration](#8-throttle-calibration)
  * [9. Track Preview](#9-track-preview)
- [Lesson 3: Test Drive DeepRacer](#lesson-3-test-drive-deepracer)
  * [1. Lesson Overview](#1-lesson-overview)
  * [2. Around the Track](#2-around-the-track)
  * [3. AWS DeepRacer workflow](#3-aws-deepracer-workflow)
  * [4. The Console and Your First Model](#4-the-console-and-your-first-model)
  * [5. The Basic Reward Function](#5-the-basic-reward-function)
  * [6. Exercise I: Training on the Console](#6-exercise-i-training-on-the-console)
  * [7. Exercise I: Task I](#7-exercise-i-task-i)
  * [8. Exercise I: Conclusion](#8-exercise-i-conclusion)
- [Lesson 4: Reinforcement Learning](#lesson-4-reinforcement-learning)
  * [1. RL and DeepRacer](#1-rl-and-deepracer)
  * [2. Machine Learning Algorithms](#2-machine-learning-algorithms)
  * [3. A Concrete Example](#3-a-concrete-example)
  * [4. RL Agents, Actions and States](#4-rl-agents-actions-and-states)
  * [5. State Transitions](#5-state-transitions)
  * [6. Discount Factors and Policies](#6-discount-factors-and-policies)
  * [7. Value Functions](#7-value-functions)
  * [8. Mapping RL to DeepRacer](#8-mapping-rl-to-deepracer)
  * [9. Other Use Cases of RL](#9-other-use-cases-of-rl)
  * [10. Lesson Review](#10-lesson-review)
- [Lesson 5: Tuning Your Model](#lesson-5-tuning-your-model)
- [Lesson 6: DeepRacer in the Real World](#lesson-6-deepracer-in-the-real-world)
- [Lesson 7: The League](#lesson-7-the-league)

<!-- tocstop -->

## Lesson 1: Welcome! Important Details on the AWS DeepRacer Scholarship

### 1. AWS DeepRacer Scholarship Challenge

## Lesson 2: Get Started with AWS DeepRacer

### 1. Intro to AWS DeepRacer
### 2. Welcome

* the car's tech specs, assembly and calibration
* the basics of reinforcement learning and its use in AWS DeepRacer
* building, training and deploying your racing model using AWS in both simulated and real-world tracks
* how to compete in the DeepRacer League

### 3. RL in AWS DeepRacer
* AWS DeepRacer:
    * is fully-autonomous
    * is a 1/18th scale racing car
    * utilizes RL to learn driving habits
* Types of machine learning include:
    * Supervised learning
    * Unsupervised learning
    * Reinforcement learning

### 4. Unboxing AWS DeepRacer
* Unboxing Recap
    *   AWS DeepRacer includes the following in its box:

        1. Car chassis (with compute and camera modules)
        2. Car body
        3. Car battery
        4. Car battery charger
        5. Car battery power adapter
        6. Compute module power bank
        7. Power bank’s connector cable
        8. Power adapter and power cord for compute module and power bank
        9. 4 pins (car chassis pins)
        10. 12 pins (spare parts)
        11. USB-A to micro USB cable

    * You can read more in the [Getting Started Guide](https://d1.awsstatic.com/deepracer/AWS-DeepRacer-Getting-Started-Guide.pdf).

### 5. Under the Hood

* Other than the vehicle chassis, the vehicle also includes:

    * a HD DeepLens camera
    * expansion ports
    * HDMI port
    * microUSB port
    * USB-C port
    * on/off switch
    * reset button
    * LEDs

### 6. DeepRacer Assembly



### 7. Steering Calibration

1. Place your car on a block (secure it with duct tape or similar) to keep it in place while the wheels move.
2. Get your vehicle’s IP address from when it was set up to use wi-fi.
3. Sign in to the AWS DeepRacer console with that IP address as instructed here.
4. Select Calibration, then Calibrate Steering Angle from the console (see here).
5. Calibrate your center steering first. Remember: Due to the concepts of Ackermann steering, only one wheel will actually be straight when you calibrate center steering.
6. Calibrate your left steering by choosing the value where your vehicle wheels will turn no further left.
7. Calibrate your right steering by choosing the value where your vehicle wheels will turn no further right.

### 8. Throttle Calibration

1. Place your car on a block (secure it with duct tape or similar) to keep it in place while the wheels move.
2. Get your vehicle’s IP address from when it was set up to use wi-fi.
3. Sign in to the AWS DeepRacer console with that IP address as instructed here.
4. Select Calibration, then Calibrate Speed from the console (see here).
5. Calibrate your stopped speed by moving the bar until the wheels are no longer moving.
6. Calibrate the forward motion by moving the bar and checking the direction the wheels turn. If they turn clockwise, the forward direction is set. If not, select the “Reverse direction” button to switch the direction the wheels turn to go forward.
7. Calibrate the forward maximum speed. Typically, it’s best not to go too high above 2 m/s, as that is the highest the simulator provides in its action space.
8. Calibrate the maximum backward speed, which should be essentially the negative value of what the maximum forward speed was set at.

### 9. Track Preview

## Lesson 3: Test Drive DeepRacer

### 1. Lesson Overview
### 2. Around the Track
### 3. AWS DeepRacer workflow
### 4. The Console and Your First Model

1. Sign into the console
2. Click the Get Started / Create Model button on the right
3. Create resources, if they aren't created yet
4. Name and describe your model
5. Choose an environment (re:Invent 2018 for now)
6. Select action space
7. Select reward function
8. Tune hyperparameters
9. Set stop condition

### 5. The Basic Reward Function

* decreasing rewards based on the vehicle being within a given marker or not

### 6. Exercise I: Training on the Console

1. Akses dan navigasikan konsol AWS DeepRacer
2. Identifikasi langkah-langkah yang digunakan untuk membangun model di konsol AWS DeepRacer
3. Gunakan fungsi hadiah dasar di AWS DeepRacer saat mengkonfigurasi model
4. Gunakan simulator AWS DeepRacer untuk melatih dan mengevaluasi suatu model

### 7. Exercise I: Task I



### 8. Exercise I: Conclusion

1. Accessed and navigated within the AWS DeepRacer console
2. Identified the steps that go into building a model in the AWS DeepRacer console
3. Used the basic reward function in AWS DeepRacer to configure a model
4. Used the AWS DeepRacer simulator to train and evaluate a model

## Lesson 4: Reinforcement Learning

### 1. RL and DeepRacer

### 2. Machine Learning Algorithms

* Supervised learning trains a model based on providing labels to each input, such as classifying between images of a bulldog and those that are not a bulldog.
* Unsupervised learning can use techniques like clustering to find relationships between different points of data, such as in detecting new types of fraud
* Reinforcement learning uses feedback from previous iterations, using trial and error, to improve

### 3. A Concrete Example

### 4. RL Agents, Actions and States

* Agent - the entity exhibiting certain behaviors (actions) based on its environment. In our case, it’s our AWS DeepRacer car.
* Actions - what the agent chooses to do at certain places in the environment, such as turning, going straight, going backward, etc. Actions can be discrete or continuous.
* States - has to do with where in the environment the agent resides (at a specific location) or with what is going on in the environment (for a robotic vacuum, perhaps that its current location is also clean). By taking actions, the agent moves from one state to a new state. States can be partial or absolute.

### 5. State Transitions

* To begin our cycle, the agent will choose an action given its starting state in the environment. It will then transition to a new state, where it will receive some reward. This will keep on in a continuous cycle of choosing a new action, moving to a new state, receiving a reward, and so on, for the rest of a given training episode.

### 6. Discount Factors and Policies

* Discount factor - determines the extent to which future rewards should contribute to the overall sum of expected rewards. At a factor of zero, this means DeepRacer would only care about the very next action and its reward. With a factor of one, it pays attention to future rewards as well.
* Policy - this determines what action the agent takes given a particular state. Policies are split between stochastic and deterministic policies. Note that policy functions are often denoted by the symbol \piπ.
    * Stochastic - determines a probability for choosing a given action in a particular state (e.g. an 80% chance to go straight, 20% chance to turn left)
    * Deterministic - directly maps actions to states.
* Convolutional neural network - a neural network whose strength is determining some output from an image or set of images. In our case, it is used with the input image from the DeepRacer vehicle (whether real or simulated).

### 7. Value Functions

* Value functions indicate which actions you should take to maximize rewards over the long-term (the expected rewards when starting from some given state). These are often represented with the capital letter VV.
* AWS DeepRacer uses the Proximal Policy Optimization (PPO) algorithm to help optimize the value function.
* Policy network (aka actor network) - decides which action to take given an input image
* Value network (aka critic network) - estimates the cumulative result given the input image

### 8. Mapping RL to DeepRacer

* Our agent is AWS DeepRacer itself, or more specifically the neural networks controlling the vehicle.
* The environment is where the agent performs its actions; in this case, the track.
* The action is what the agent decides to do based on the current state - changing speed, turning, etc.
* The state is a given point in time where AWS DeepRacer finds itself in the environment.
* The reward is feedback given to the agent based on its action from the previous state. It is rewarded for doing well or penalized for doing poorly.

### 9. Other Use Cases of RL

### 10. Lesson Review

* You learned about how RL differs from supervised and unsupervised learning
* You walked through an example of how a RL-trained agent behaves
* You went in depth on the main aspects of a RL model, such as agents, actions, environments, states and rewards
* You saw how each of these aspects apply to AWS DeepRacer
* Finally, you investigated some of the other use cases of RL

## Lesson 5: Tuning Your Model
## Lesson 6: DeepRacer in the Real World
## Lesson 7: The League