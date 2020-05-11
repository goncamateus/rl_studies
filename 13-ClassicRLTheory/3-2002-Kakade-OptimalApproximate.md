# Title : Approximately Optimal Approximate Reinforcement Learning

# Author: Kakade and Langford
### Filiation: Gatsby UCL
### Publication at: ICML
Link [ Approximately Optimal Approximate Reinforcement Learning][link]

#### Gerenal Content

Presents the consevative policy iteration algorithm which finds an approximately optimal policy and
an approximate greedy policy chooser

The greedy policy chooser outpus a policy that maximizes the state-action values

The greedy policy chooser can be obtained using standard value functions approximation techniques

the algorithm guarantees:
* to improve a performance metric
* it terminates in a small number of timesteps
* it returns an approximetely optimal policy

The guarantees don't depend on the size of the problem's state-space but only on the quality
of the greedy policy chooser

#### Key take-aways

Begin theory what we will use in algorithms such as PPO
Inteds to address the "problem" of exploring and exploiting in grandient policy methods (thus,
causing the necessity of a unreasanable large number of samples).


#### Keypoints

Assumes the existence of:
- Restart Distribution : allows the agent to obtain it's next state
- Greedy Policy Chooser : a black box that returns a policy that on average chooses actions
with the largest advantages with respect to the currently policy

Such an algorithm as proposed is proven in the paper that converges in a "small" number of
steps and returns an approximate optimal policy. Independently of the state space size

By using a uniform restart distribution it can obiviate the need for explicit exploration.

The given algorithm is not interested in the quality of the policy in a asymptotic way. It
is interested in a policy found in a realistic amount of time. It aims in three questions:
- 1) Is there a performance metric that improves every time step?
- 2) How difficult is to verify if an update improves this metric?
- 3) after a number of update what performance level is obtained?

Approximate value methos can neither responde any of these questions as they don't gruarantee
improvement and a performance measure isn't well defined

Policy Gradients Methods follow the gradient ascent of the performance measures, which answers
the question 1. The lack of exploration in gradient methods translates into requiring a large
number of samples to accurately estimate the gradient direction (without this estimate
question 2 cannot be properly answered). Question 3 was not answered by the time.



#### Observations and Questions

What is small number of steps?
The observation that by using a uniform restart distribution makes the exploration less
important for the algorithm is really clever.

How can we define improvements every step in value-based rl and policy gradient methods?

#### References



