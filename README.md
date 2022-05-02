# Reinforcement Learning for Traffic Light Control
![ACM Research Poster-Reinforcement Learning Traffic Light Control pptx](https://user-images.githubusercontent.com/77949696/166319351-cee78c38-8b70-4ea6-8dc1-eb2c83857491.png)

## Problem Overview
<img src="https://user-images.githubusercontent.com/77949696/166315910-40763888-a755-4641-948b-b458f304903c.png" width="300">

It is estimated that the average american will lose about 97 hours every year as a result of traffic congestion, which has significant financial effects. If you take a look at this graph provided by INRIX (the world leader in mobility analytics), you can see that the congestion cost per driver, the cost of congestion which takes into account the increase in fuel wasted, negative effects of pollution, and other factors, has hit record highs and is only increasing. Our goal is to reduce this, to mitigate the effects of traffic congestion by exploring the effectiveness of applying reinforcement learning to traffic light signal control.


### Timeline
- Explore Reinforcement Learning Approaches
- Configure Simulation Environment
- Data preprocessing
- Model development and training
- Results Analysis

## Approach
- We chose to apply reinforcement learning versus another method of machine learning because we can it’s very straightforward to reward a desired behavior that for example reduces vehicle wait time and punish an undesired behavior that increases vehicle wait time.
- There are numerous types of reinforcement learning, such as State-Action-Result-State-Action (SARSA) and Deep Q-Networks (DQN). However, Q-learning was chosen as method to apply.



### Q-Learning
<img src="https://user-images.githubusercontent.com/77949696/166317007-0b45c637-1df2-4df9-845c-69e42672f659.png" width="200">

- Form of reinforcement learning that seeks to learn a policy which maximizes the total reward
- Q values are stored in a Q-table, and are referenced by the model where it selects an action and stored the reward of that action
- The reward function that we used calculates the reward by calculating the change in cumulative vehicle delay



### Simulation of Urban MObility (SUMO)
<img src="https://user-images.githubusercontent.com/77949696/166318037-a0ec4b26-9197-45b9-b9a5-64b01a64d12c.png" width="600">
<img src="https://user-images.githubusercontent.com/77949696/166319015-614ac820-54b2-4200-9e21-739e7de1b475.png" width="400">

- ***S***imulation of ***U***rban ***MO***bility is an open source, portable, microscopic and continuous multi-modal traffic simulation package designed to handle large networks.
- It’s also cited as being traditionally used in traffic signal control studies, so we determined it was the best way to create our simulation environment.


## Data Preprocessing
Our initial goal was to have our model train on real world data and compare its optimizations to real world performances. However, there were too many difficulties in Data Preprocessing. There were too much missing data, issues with converting data to vehicle routes, and difficulty building the environment for the datasets. Because of these issues, we sticked with route generated data to train our model.

### Developing the Model
- Uses ***TraCI (Traffic Control Interface)***, a library in SUMO that allows for the controlling of the traffic signals

<img src="https://user-images.githubusercontent.com/77949696/166320864-b1a8ba32-3259-4af4-9137-479a9fad1b37.png" width="450">

- Action selection determined by an ***epsilon-greedy algorithm*** (picture above)
  - Balances exploration and exploitation
  - Initial epsilon value for the experiment was set to be 0.05


## Results
<img src="https://user-images.githubusercontent.com/77949696/166319871-a3a70a3d-dd31-44db-b5d8-26da0ed79f8b.png" width="400">


## Next steps
- Explore alternative reinforcement learning methods (SARSA/DQN)
- Examine the performance of the model in comparison to real world data
- Experiment on more complex intersections (more lanes, intersections connected to one another, etc.)


## Contributors
- [Fiona Burleson](https://github.com/fionarb)
- [Justin Doan](https://github.com/justin-doan)
- [James Han](https://github.com/notJamesHan) 
- Cassandra Lauzon
- [Ryan Aspenleiter](https://github.com/RyanAspen) - Research Lead
- Dr. Yongwan Chun - Faculty Advisor
