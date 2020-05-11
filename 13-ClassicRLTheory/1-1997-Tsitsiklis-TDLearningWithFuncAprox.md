# Title : An Analysis of Temporal-Difference Learning with Function Approximation

# Author: sitsiklis and Van Roy(1997)
### Filiation: MIT
### Publication at: IEEE Transactions on automatic Control
Link [An Analysis of Temporal-Difference Learning with Function Approximation][http://web.mit.edu/jnt/www/Papers/J063-97-bvr-td.pdf]

#### Gerenal Content

Discuss the impact of using temporal difference learning algorithm to approximate
the future costs function of a infinite discounted Markov Chain.

The algorithm  analyzed updates parameters of a linear function approximator online.

Runs the algorithm on a single trajectory over an irreducible aperiodic Markov chain
with finites or infinites state space.

The paper provides a proof of convergence, a characterization of the limit of convergence,
and a bound on the resulting approximation error.

It prooves divergence may occur when updates are not based in trajectories of the
Markov chain. (what does it mean?)

After the paper analyzes the performance of the algorithm on  online
updating non-linear function approximator. It shows how TD can diverge in this cases.

#### Key take-aways

* The paper is of easy reading, well writting and concise. May follow these practices
when writting scientifically

* Td learning algorithm may diverge if states are sampled randomly (this implies
one must be careful with experince replay?)

#### Keypoints

* Main Problem: How to estimate the future costs (or rewards) of a system.
* If states are sampled from distributions independent of the dynamics of the Markov
chain of interest, the algorithm may diverge.
* Convergence is always guaranteed for linear function approximators if states are
sampled according to the steady-state probabilites (online sampling).

#### Observations and Questions

* The paper implies samples must be taken of the sequence of visited states,
but why is experience replay indicated since it does take samples from a random
distribution? (i know td is not q-learning but is similar right?)


#### References



