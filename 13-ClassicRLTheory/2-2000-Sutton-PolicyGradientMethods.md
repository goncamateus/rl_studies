# Title : Policy Gradient Methods for Reinforcement Learning with Function Approximation

# Author: Sutton et al
### Filiation: AT&T Labs
### Publication at: NiPS
Link [Policy Gradient Methods for Reinforcement Learning with Function Approximation][https://papers.nips.cc/paper/1713-policy-gradient-methods-for-reinforcement-learning-with-function-approximation.pdf]

#### Gerenal Content

Given the theoretic proofs against using a value function and determining a policy from it. Sutton
explores the use of an approximation function as the policy itself (on-policy/actor-critic).

The Policy is updated following the gradient of the expected reward w.r.t the policy function
parameters.

Main contribution of this paper is to show that the gradient of expected reward can be written
in a form suitable for estimation from experience, aided by an aproximation action-value funcion (Q)
or advantage function. Prooves for the first time that a version policy interation with arbitrary
differentiable function approximation (ex: Neural nets) is convergent to a local optimal policy

#### Key take-aways

Short paper with high relevance of every part
Sutton here seems to give proof that action-critic networks will converge
Stabilishes the Policy Gradient Theorem

Shows convergence of policy gradient algorithm for arbitrary policy classes

#### Keypoints

Given that the proof is about local optimal, the method itself does not have means to deal
with it. I believe this details are let to the approximator function to deal (like momentum
im neural nets)

Unlike in value function approaches, where a small change in some action's value can cause
a complete (discontinuos) change on the outcome, in policy gradient, a small change in
parameters cause small changes in the policy and, consequently, in the state-visitation
distribution

Show that actor-critic approach are always guaranteed to converge to local optimum.

The optimial solution to a control problem is a stochastic controller

#### Observations and Questions


#### References



