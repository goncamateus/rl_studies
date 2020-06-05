# Title : Reinforcement learning of motor skills with policy gradients

# Author: Peters and Schaal
### Filiation: Gatsby University of Southern California
### Publication at: Neural Networks
Link [A Natural Policy Gradient][https://www.sciencedirect.com/science/article/abs/pii/S0893608008000701?via%3Dihub]

#### Gerenal Content

The studies here intends to apply at the time recent developments in reinforcement learning to
obtain a robotic human-like behavior of learning by trial-and-error

The first part show how motor primitives are suitable to be used to learn control policies

Secondly, motor primitives are combined with, at the time, state of art stochastic policy
learning.

The paper show that the Episodic Natural Actor-Critic algorithm outperforms the others
stochastic policy learning methods

They test the algorithm in the domain of hitting a baseball with an anthropomorphic arm

#### Key take-aways

Has a great explanation of the general policy gradient problem sec 1 - 4

#### Keypoints

Adds two components to the traditional reinforcement learning framework:
- A domain-specific policy representation for motor skills
- RL algorithms that work efficiently in the domain and scale to high dimension
continous domain as humanoid robots

The problem of value based rl is that they do not guaratees improvement in policy
by updating the parameters, which may lead the robot to harzardous episodes

There are two approaches of policy gradients for motor primitives
- Finite difference methods: generate a delta in paramaters and with this new
policy's roll-out estimate the gradient of the objecite. How to generate the delta?
bad deltas leads to unstability
- Likelihood ratio gradient methods: faster theoretical convergence than previous.
Estimates the gradient based only on the policy and the experienced roll-outs' states
and rewards. No need for genereting delta as in finite difference. A single roll-out
can be sufficient for an unbiased gradient estimate. This approach has yielded the
best results in real-world robot motor learning results.

* Likelihood ratio gradient methods:
- Vanilla
- Natural Gradient Methods

#### Observations and Questions


#### References



