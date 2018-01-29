
# 601.765 Machine Learning: Linguistic & Sequence Modeling

* **Lectures:** 3-3:50pm MWF, in Hackerman 320.
  * Sometimes we may have to do 3-4:15 but this will be announced in advance.
* **Instructors:** Jason Eisner, Ryan Cotterell
  * **Office hours:** 4-4:30pm after class, or by appointment.
* **TA:** Matthew Francis-Landau
  * **Office hours:** TBA
* **Discussion site:** [https://piazza.com/class/jd0fhovutom2kf](https://piazza.com/class/jd0fhovutom2kf)
* **Email:** cs765-staff at cs.jhu.edu
* **Class notes:**
  * [Formalisms and terminology](https://github.com/seq2class/scribe-notes/raw/master/formalisms.pdf)
  * [Scribe Notes](https://seq2class.github.io/scribe-notes/)
    * [LaTeX repo](https://github.com/seq2class/scribe-notes)
    * [Sign up to Scribe](https://github.com/seq2class/scribe-notes/wiki/Scribe-notes-sign-up)
  * Readings (TBA)
* **Video recordings:** TBA

## Course description

This course surveys formal ingredients that are used to build structured models of character and word sequences. We will unpack recent deep learning architectures that consider various kinds of latent structure, and see how they draw on earlier work in structured prediction, dimensionality reduction, Bayesian nonparametrics, multi-task learning, etc. We will also examine a range of strategies used for inference and learning in these models. Students will be expected to read recent papers and carry out a research project. [Applications or Analysis]

Prerequisites: EN.600/601.465/665 or permission. Prior coursework in statistics or machine learning is recommended. Students may wish to prepare for their choice of research project by taking EN.601.382 Deep Learning Lab at the same time.

## Requirements (details TBA soon)

* Scribing
* Homeworks
* Final project
* Tests (midterm and final?)

* Class participation
* Reading papers

## Topic list

1. Introduction
2. Sequence labeling as a canonical problem
3. Notation and statistical background
4. Algorithmic background: Paths in graphs
5. Classical sequence labeling models
6. Beyond dynamic programming: Approximation algorithms
7. Feature / architecture engineering
8. Neuralization
9. Word embeddings
10. Optimization methods
11. Model selection
12. Deep generative models
13. Beyond sequences: Distributions over other discrete structures
14. Transition systems for parsing
15. Integration over hidden variables
16. Reinforcement learning
17. Continuous generalizations
18. Exchangeability
19. Hierarchical modeling and types vs. tokens
20. Other possible topics:
    * Lambek calculus / CCG / automata / other models of grammaticality
    * Spectral learning
    * Structure learning

# Recurring themes

* Training objectives
  * Joint vs. conditional
  * Loss-infused training (train a policy) vs. loss-infused decoding (train a model)
  * Value-based vs. policy-basd
  * Forms of regularization
  * Smooth vs. non-smooth objectives
  * Convex vs. non-convex objectives
* Inference objectives
  * Maximization vs. summation; annealing
	* Search and sampling
	* Dual decomposition (for maximization)
    * Variational approximation (for summation)
* Modeling schemes
  * Global vs. local - and how local?
  * Graph-based vs. transition-based (= subgraph features vs. history-based features)
  * Domain knowledge vs. generic architectures
* Decomposability
  * Dynamic programming vs. approximations
  * Lookahead vs. heuristics
* Types vs. tokens
  * Embeddings
  * Weighting the training data
  * External resources
* Computational tricks of the trade and implementation know-how
