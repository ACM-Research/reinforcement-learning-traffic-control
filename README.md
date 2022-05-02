# Reinforcement Learning For Traffic Light Control

## Problem Overview
![image](https://user-images.githubusercontent.com/77949696/166315910-40763888-a755-4641-948b-b458f304903c.png)
It is estimated that the average american will lose about 97 hours every year as a result of traffic congestion, which has significant financial effects. If you take a look at this graph provided by INRIX (the world leader in mobility analytics), you can see that the congestion cost per driver, the cost of congestion which takes into account the increase in fuel wasted, negative effects of pollution, and other factors, has hit record highs and is only increasing. Our goal is to reduce this, to mitigate the effects of traffic congestion by exploring the effectiveness of applying reinforcement learning to traffic light signal control.


## Timeline
- Explore Reinforcement Learning Approaches
- Configure Simulation Environment
- Data preprocessing
- Model development and training
- Results Analysis

## Approach
- We chose to apply reinforcement learning versus another method of machine learning because we can it’s very straightforward to reward a desired behavior that for example reduces vehicle wait time and punish an undesired behavior that increases vehicle wait time.
- There are numerous types of reinforcement learning, such as State-Action-Result-State-Action (SARSA) and Deep Q-Networks (DQN). However, Q-learning was chosen as method to apply.

## Q-Learning
![image](https://user-images.githubusercontent.com/77949696/166317007-0b45c637-1df2-4df9-845c-69e42672f659.png)
- Form of reinforcement learning that seeks to learn a policy which maximizes the total reward
- Q values are stored in a Q-table, and are referenced by the model where it selects an action and stored the reward of that action
- The reward function that we used calculates the reward by calculating the change in cumulative vehicle delay

## Simulation of Urban MObility (SUMO)
![image](https://user-images.githubusercontent.com/77949696/166317702-8d30e19c-f982-4ccb-b3ce-0bc807b58931.png)
- Simulation of Urban MObility is an open source, portable, microscopic and continuous multi-modal traffic simulation package designed to handle large networks.
- It’s also cited as being traditionally used in traffic signal control studies, so we determined it was the best way to create our simulation environment


## Contributors
- [Fiona Burleson](https://github.com/fionarb)
- [Justin Doan](https://github.com/justin-doan)
- [James Han](https://github.com/notJamesHan) 
- Cassandra Lauzon
- [Ryan Aspenleiter](https://github.com/RyanAspen) - Research Lead
- Dr. Yangwan Chun - Faculty Advisor
