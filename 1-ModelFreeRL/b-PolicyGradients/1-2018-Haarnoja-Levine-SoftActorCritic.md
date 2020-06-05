# Title : Soft Actor Critic: Off-Policy Maximum Entropy Deep RL with a Stochastic Actor

# Author: Haarnoja and Sergey Levine(2018)
### Filiation: UC Berkley
### Publication at: arxiv
Link [Soft Actor Critic: Off-Policy Maximum Entropy Deep RL with a Stochastic Actor][https://arxiv.org/abs/1801.01290]

#### Gerenal Content

Model free rl suffe two major challenges:
* High sample complexity
* Brittle convergence properties (meticulous parameter tuning)

In the paper the authors introduces a new off-policy actor-critic deep RL algorithm
base on the maximum entropy reinforcement learning framework.

In the maximum entropy framework the actor aims to maximize expected reward while
maximizing entropy. In other words, the actor tries to succeed while acting as
randomly as possibly.

The proposed algorithm achieves state-of-art performance in continuous control
benchmark tasks. The algorithm is specially good in high dimension tasks. The
algorithm also has great convergence results with differents seeds.

#### Key take-aways

Maximum Entropy (ME) framework was used in diverse situations before but was
never used in a actor-critic sceneario. Thus, they suffer from the respective
paradigms policy:
* on-policy - poor sample efficiency
* off-policy - complex approximate inference in continuos action spaces

The success of the article is comparable with the success of DDPG.
DDPG and SAC are very similar, maximum entropy aside.

Actor-critic algorithms are typically derived from policy iteration which is:
* Policy Evaluation - computing the value of a policy (Critic)
* Policy Improvement - using the value function to obtain a better policy (actor)
It's impractical to run each step above to convergence, instead they are optimized
jointly.

Efforts to increase sample efficiency while reatining robustness:
* Incorporating off-policy samples
* higher order variance reduction techniques* (what is this?)

In complex, high-dimensional tasks on-policy policy gradient methods tend to produce
the best results

Sac combine soff-policy actor-critic with a stochastic actor

Stochastic actor: instead of learning the actual actions, the actor learns a mean
e variance of the action gaussian.

The maximum entropy framework is known to favor stochastic policies

The soft policy iteration is guaranteed to find the optimal solution in the tabular
case. SAC is a generalization of the algorithm to the contiunous space.

Results:
* Stability: reward scaling is the "only" important hyperparameter to be tunned
* Stability between runs is improved by stochastic actions taking
* Evaluation must be done deterministacally for better results (mean of action)
* Results: is remarkably good in high dimensional spaces environments

Conclusions

`Our results suggest that stochastic, entropy maximizing
reinforcement learning algorithms can provide a promising
avenue for improved robustness and stability, and further
exploration of maximum entropy methods, including meth-
ods that incorporate second order information (e.g., trust
regions (Schulman et al., 2015)) or more expressive policy
classes is an exciting avenue for future work.`

#### Keypoints

On-policy learning is the main cause of poor sample efficiency of deep RL methods.
* such as: TRPO, PPO, A3C, etc
These algorithms require new samples to be collected for each gradient step.

Off-policy algorithms aims to reuse past experiences, thus, reducing the need
for new samples. Unfortunatelly the use of off-policy algorithms and high-dimension,
nonlinear function approximation with neural networks presents a major challenge
for convergence and stability (worse in continuos action/state space).

In the continuous settings, one sucessful algorithm to be used is DDPG, it provides
sample efficiency but it's difficult to use, due to hyperparameter sensitivity and
extreme brittleness

Maximum entropy(ME) formulation provides a substancial improvement in exploration and
robusteness.
ME policies are robust for model and estimation errors. they improve exploration by
acquire diverse behavior.

Prior work has used ME framework in on-policy learning as well as off-policy based
on soft Q-learning.

The SAC algorithm provides sample efficiency and stability.

Many actor-critic algorithms before used entropy of the policy as a regularizer,
instead of maximizing it.

Sac combines off-policy actor-critic with a stochastic actor, aiming to maximize the
entropy of the policy


#### Observations and Questions

Attention to Twin-delayed deep deterministic policy gradient algorithm (TD3), that
is a deterministic algorithm that substantially improves on DDPG

Higher order variance reduction techniques to increase samples efficiency, how
does it work?


#### References


#### Future Work

* Investigate second order information with maximum entropy and sthocastic (ex: trust regions)
* Apply the conclusions learned in this paper to ddpg marl or other marl algorithm



