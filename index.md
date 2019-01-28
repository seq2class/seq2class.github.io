# 601.765 Machine Learning: Linguistic & Sequence Modeling

## Spring 2019

## Announcements

* The first day of class is Monday, Jan 28.  See you there!
* Please fill out the [questionnaire](https://docs.google.com/forms/d/e/1FAIpQLSelKHO6-6c2funbIIFSnZ8WGzZ_9IT5DeRK_XQEumqwWUYvow/viewform).

<!-- * Homework 1 has been posted [here](https://piazza.com/class/jd0fhovutom2kf?cid=14).  Due 2/19 at 2:00 PM -->

## Administration

* **Lectures:** 3-4pm MWF, in Hackerman 320.
  * Sometimes we may have to do 3-4:15 but this will be announced in advance.
* **Instructor:** Jason Eisner
  * **Office hours:** 4-4:30pm after class, or by appointment.
* **TA:** Sebastian Mielke
  * **Office hours:** TBA
* **Email:** cs765-staff at cs.jhu.edu
* **Discussion site:** [https://piazza.com/jhu/spring2019/601765/]
* **Class notes:**
  * [Formalisms and terminology](https://github.com/seq2class/scribe-notes/raw/master/formalisms.pdf)
  * [Scribe Notes](https://seq2class.github.io/scribe-notes/)
    * [LaTeX repo](https://github.com/seq2class/scribe-notes)
    * [Sign up to Scribe](https://github.com/seq2class/scribe-notes/wiki/Scribe-notes-sign-up)
  * Readings (TBA)
* **Video lectures:** [via Blackboard](https://blackboard.jhu.edu/webapps/ppto-PanoptoCourseTool-bb_bb60/Content.jsp?course_id=_155622_1&mode=cpview)

## Homework

Homeworks will be posted here.  We will probably have 4 homeworks (plus a term project).

### Old homeworks (from Spring 2018)

Last year's homework assignments are listed here for reference.  You can expect some similar assignments this year.

* [Homework 1](https://github.com/seq2class/assignment1): Slow general algorithms for sequence labeling
* [Homework 2](https://github.com/seq2class/assignment2): Efficient finite-state methods
* [Homework 3](https://github.com/seq2class/assignment3): Neural models

## Course overview

_Catalog description_: This course surveys formal ingredients that are used to build structured models of character and word sequences. We will unpack recent deep learning architectures that consider various kinds of latent structure, and see how they draw on earlier work in structured prediction, dimensionality reduction, Bayesian nonparametrics, multi-task learning, etc. We will also examine a range of strategies used for inference and learning in these models. Students will be expected to read recent papers and carry out a research project. [Applications or Analysis]

_Prerequisites:_ EN.600/601.465/665 or permission. Prior coursework in statistics or machine learning is recommended. Students may wish to prepare for their choice of research project by taking EN.601.382 Deep Learning Lab at the same time.

_Remarks:_
* The focus of the class is on understanding the space of *good options* for designing probabilistic sequence models and computing with them.
* We will discuss the *qualitative* advantages and disadvantages of different options.  Our goal is not to teach you exactly how today's top-ranked system works, but rather to give you a toolbox for understanding and creating system designs.
* This class builds on the dynamic programming algorithms and log-linear models covered in [NLP](http://cs.jhu.edu/~jason/465).  We will primarily extend to various neural ("log-nonlinear") models, some of which allow dynamic programming.
* As this is a graduate class, the lecture style will be a bit more improvisational than in [NLP](http://cs.jhu.edu/~jason/465). The class is also still under development. We will probably only cover a subset of the topics on the syllabus.

## Requirements (details TBA)

* Attending lectures
* Scribing? (i.e., drafting lecture notes)
* Reading papers?
* Homeworks
* Midterm exam?
* Final exam
* Final project

## Topic list

### Setting the stage

<ol start="1">
<li>Overview</li>
<li>Sequence labeling as a canonical problem</li>
</ol>

### Classical methods

<ol start="3">
<li> Notation and statistical background</li>
<li>Algorithmic background: Paths in graphs</li>
<li>Classical sequence labeling models</li>
<li>Graphical models and belief propagation</li>
</ol>

### Richer scoring functions

<ol start="6">
<li>Beyond dynamic programming: Approximation algorithms</li>
<li>Feature / architecture engineering</li>
<li>Neuralization</li>
<li>Word embeddings</li>
<li>Backprop and optimization methods</li>
<li>Hyperparameter tuning (model selection)</li>
<li>Deep generative models</li>
</ol>

### Beyond sequence labeling

<ol start="13">
<li>Distributions over other discrete structures</li>
<li>Transition systems for parsing</li>
<li>Integration over hidden variables</li>
<li>Reinforcement learning</li>
<li>Continuous generalizations</li>
<ul>
<li>Kalman filters</li>
<li>Poisson and Hawkes processes</li>
<li>Gaussian processes</li>
</ul>
<li>Exchangeability</li>
<ul>
<li>Dirichlet processes</li>
</ul>
<li>Hierarchical modeling</li>
<ul>
<li>Types vs. tokens</li>
<li>Infinite Gaussian mixture model</li>
<li>Hierarchical Pitman-Yor language model</li>
<li>Infinite HMM</li>
</ul>
</ol>

### Other possible topics (time permitting)

<ol start="20">
<li>Lambek calculus / CCG / automata / other models of grammaticality</li>
<li>Spectral learning</li>
<li>Structure learning</li>
</ol>

## Recurring themes

In some sense, the point of the course is to explicitly show you the
collection of design choices that you face when building probabilistic
reasoning systems.  Your choices will affect (1) how well your models
fit the theory and the data, (2) the computational complexity of inference
and training, and (3) the difficulty of implementing the system.

* Training objectives
  * Joint vs. conditional
  * Loss-infused training (train a policy) vs. loss-infused decoding (train a model)
  * Forms of regularization
  * Smooth vs. non-smooth objectives
  * Convex vs. non-convex objectives
  * End-to-end vs. pipelined training
* Inference objectives
  * Maximization vs. summation; annealing
	* Search and sampling
	* Dual decomposition (for maximization)
    * Variational approximation (for summation)
* Modeling schemes
  * Global vs. local - and how local?  (= lookahead vs. heuristics)
  * Graph-based vs. transition-based (= subgraph features vs. history-based features)
  * Tractable vs. faithful models
  * Domain knowledge vs. generic architectures
* Types vs. tokens
  * Model structure
  * Weighting the training data
* Computational tricks of the trade and implementation know-how
