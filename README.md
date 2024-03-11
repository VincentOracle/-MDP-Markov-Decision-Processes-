# What Is the Markov Decision Process?
A Markov decision process (MDP) is defined as a stochastic decision-making process that uses a mathematical framework to model the decision-making of a dynamic system in scenarios where the results are either random or controlled by a decision maker, which makes sequential decisions over time.

 It is used in scenarios where the results are either random or controlled by a decision maker, which makes sequential decisions over time. MDPs evaluate which actions the decision maker should take considering the current state and environment of the system.

MDPs rely on variables such as the environment, agent’s actions, and rewards to decide the system’s next optimal action. They are classified into four types — finite, infinite, continuous, or discrete — depending on various factors such as sets of actions, available states, and the decision-making frequency.

MDPs have been around since the early part of the 1950s. The name Markov refers to the Russian mathematician Andrey Markov who played a pivotal role in shaping stochastic processes. In its initial days, MDPs were known to solve issues related to inventory management and control, queuing optimization, and routing matters. Today, MDPs find applications in studying optimization problems via dynamic programming, robotics, automatic control, economics, manufacturing, etc.

In artificial intelligence, MDPs model sequential decision-making scenarios with probabilistic dynamics. They are used to design intelligent machines or agents that need to function longer in an environment where actions can yield uncertain results. 

# How Does the Markov Decision Process Work?
The MDP model operates by using key elements such as the agent, states, actions, rewards, and optimal policies. The agent refers to a system responsible for making decisions and performing actions. It operates in an environment that details the various states that the agent is in while it transitions from one state to another. MDP defines the mechanism of how certain states and an agent’s actions lead to the other states. Moreover, the agent receives rewards depending on the action it performs and the state it attains (current state). The policy for the MDP model reveals the agent’s following action depending on its current state.

The MDP framework has the following key components:

S: states (s ∈ S)
A: Actions (a ∈ A)
P (St+1|st.at): Transition probabilities
R (s): Reward

The graphical representation of the MDP model is as follows:

![image](https://github.com/VincentOracle/-MDP-Markov-Decision-Processes-/assets/104081669/49e31372-55ae-4b6d-9f9d-a445b2131e14)

The MDP model uses the Markov Property, which states that the future can be determined only from the present state that encapsulates all the necessary information from the past. The Markov Property can be evaluated by using this equation:

P[St+1|St] = P[St+1 |S1,S2,S3……St]

According to this equation, the probability of the next state (P[St+1]) given the present state (St) is given by the next state’s probability (P[St+1]) considering all the previous states (S1,S2,S3……St). This implies that MDP uses only the present/current state to evaluate the next actions without any dependencies on previous states or actions.

# The policy and value function
The policy (Π) is known to determine the agent’s optimal action given the current state so that it gains the maximum reward. In simple words, it associates actions with states.

Π: S –> A

To determine the best policy, it is essential to define the returns that reveal the agent’s rewards at every state. As a result, the horizon method is not preferred to focus on short-term or long term-rewards. Instead, a variable termed ‘discounted factor (γ)’ is introduced. The rule says if γ has values that are closer to zero, then the immediate rewards are prioritized. Subsequently, if γ reveals values closer to one, then the focus shifts to long-term rewards. Hence, the discounted infinite-horizon method is key to revealing the best policy.

![image](https://github.com/VincentOracle/-MDP-Markov-Decision-Processes-/assets/104081669/165aa9c7-3ad6-4ac0-bcd8-c4bb0f7c286d)


The value function V(s) identifies the reward return at each specific state. Its formula is characterized by the expected sum of discounted future rewards:


The value function V(s) identifies the reward return at each specific state. Its formula is characterized by the expected sum of discounted future rewards:

MDP model1
The value function can be divided into two components: the reward of the current state and the discounted reward value of the next state. This breakdown derives Bellman’s equation, as shown below:

![image](https://github.com/VincentOracle/-MDP-Markov-Decision-Processes-/assets/104081669/5af9005d-8d91-4b9d-b635-cc5dc28ed9bf)


MDP model2
Here, it is worth noting that the agent’s actions and rewards vary based on the policy. This implies that the value function is specific to a policy.

Optimal value function can be solved with the help of iterative methods such as Monte-Carlo evaluations, dynamic programming, or temporal-difference learning. The policy that chooses the maximum optimal value while considering the present state is referred to as the optimal policy. Mathematically, it is represented by the following equation:

![image](https://github.com/VincentOracle/-MDP-Markov-Decision-Processes-/assets/104081669/8e7b5f8c-7838-4c7b-bf8c-905b3deb90fd)



MDP model3
Thus, the policy is a consequence of the current state wherein, at each time step, a new policy is evaluated based on the current state information. It is enabled through several methods, such as policy iteration, Q-learning, value iteration, and linear programming to solve the optimal policy function.

# Examples of the Markov Decision Process
MDPs have contributed significantly across several application domains, such as computer science, electrical engineering, manufacturing, operations research, finance and economics, telecommunications, and so on.

## Listed here are a few simple examples where MDP continues to play an imminent role:

### 1. Routing problems
MDP-based sequential decision-making is used to address routing problems such as those revealed in the traveling salesman problem (TSP). TSP can be broken down into the following components:

Salesman = agent, 
Routes available = the actions that the agent can take while in the current state, 
Rewards = the costs of taking the specific routes, and 
Goal = the optimal policy that lowers the overall cost for the entire duration of the trip.
### 2. Managing maintenance and repair of dynamic systems
The maintenance and repair problems apply to dynamic systems like cars, buses, or trucks that deteriorate over time due to the actions in varied environments. The decisions, in this case, may refer to the act of doing nothing, performing repair tasks, or replacing the critical components of the vehicle. The formulation of this problem under MDP enables the system to choose actions that help minimize the vehicle’s maintenance cost over its lifespan.

### 3. Designing intelligent machines
Advancements in AI and machine learning have resulted in the extensive use of MDPs in robotics, complex autonomous systems, autonomous vehicles, automated systems, and so on. MDPs are used within reinforcement learning models that teach robots and machines how to autonomously learn and accomplish specific tasks.

For example, Google’s subsidiary, DeepMind Technologies, combines the MDP framework with neural networks and trains computing systems to play Atari games better than humans. The company has further used MDPs to teach machines to play board games such as AlphaGo. DeepMind Technologies has also exploited the MDP framework to teach simulated robots how to walk and run.

### 4. Designing quiz games
MDPs have been widely used to design quiz games with certain levels. At each level, a question is asked, which, if answered correctly, generates a monetary reward. As the level increases, the questions become tougher and attract higher rewards.

In quiz games, if the participant plays well and answers all questions correctly, then they get the reward for it and also a chance to decide whether to play the quiz from thereon or quit the game. If the participant quits, he can possibly keep all the earned rewards. However, if he chooses to play and fails to answer the question correctly at a certain level, he loses all the accumulated rewards. The goal of such games is to evaluate the actions of playing or quitting while maximizing the rewards.

### 5. Managing wait time at a traffic intersection
MDPs help in deciding the time duration of traffic lights. The objective here is to maximize the number of vehicles that can pass through traffic intersections while keeping a check on their wait times. It can be a two-way intersection where the traffic can flow in either direction, such as west or south, and so on. It is also assumed that the system has data on the number of vehicles approaching the intersection via sensors. The traffic lights, in this case, are red and green. Here, each step takes a few seconds (2 or 5). With MDPs, you can decide whether or not to change the traffic lights depending on the vehicles at the intersection and their wait times.

### 6. Determining the number of patients to admit to a hospital
Every day, a certain number of patients visit the hospital for various reasons. The hospital then has to decide how many patients it can admit while considering factors such as:

the number of patients already admitted, 
the number of beds available, and 
the total number of patients that recover and get discharged daily. 
While determining the number of patients to admit, the hospital also intends to maximize the number of patients that recover over a certain period. Both these objectives can be achieved by formulating MDPs for them.

Apart from the above real-life examples, MDPs are vital for optimizing telecommunication protocols, streamlining stock trading, and fine-tuning queue control in manufacturing sectors.

## Real-world example to understand the working of MDP better

We have a problem where we need to decide whether the tribes should go deer hunting or not in a nearby forest to ensure long-term returns. Each deer generates a fixed return. However, if the tribes hunt beyond a limit, it can result in a lower yield next year. Hence, we need to determine the optimum portion of deer that can be caught while maximizing the return over a longer period.

The problem statement can be simplified in this case: whether to hunt a certain portion of deer or not. In the context of MDP, the problem can be expressed as follows:

##### States:
The number of deer available in the forest in the year under consideration. The four states include empty, low, medium, and high, which are defined as follows:
Empty: No deer available to hunt
Low: Available deer count is below a threshold t_1
Medium: Available deer count is between t_1 and t_2
High: Available deer count is above a threshold t_2
##### Actions:
Actions include go_hunt and no_hunting, where go_hunt implies catching certain proportions of deer. It is important to note that for the empty state, the only possible action is no_hunting.

##### Rewards:
Hunting at each state generates rewards of some kind. The rewards for hunting at different states, such as state low, medium, and high, maybe $5K, $50K, and $100k, respectively. Moreover, if the action results in an empty state, the reward is -$200K. This is due to the required e-breeding of new deer, which involves time and money.

##### State transitions: 
Hunting in a state causes the transition to a state with fewer deer. Subsequently, the action of no_hunting causes the transition to a state with more deer, except for the ‘high’ state.
