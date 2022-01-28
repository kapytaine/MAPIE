.. title:: Theoretical Description for classification : contents

.. _theoretical_description_classification:

==========================================
Theoretical Description for classification
==========================================

The :class:`mapie.regression.MapieClassifier` class implements several conformal methods
for estimating predictions sets, i.e. a set of possibilities that include the true label
with a given confidence level.
The full-conformal methods being computationally intractable, we will focus on the split-
and cross-conformal methods. 

Before describing the methods, let's briefly present the mathematical setting.
For a classification problem in a standard independent and identically distributed
(i.i.d) case, our training data :math:`(X, Y) = \{(x_1, y_1), \ldots, (x_n, y_n)\}`
has an unknown distribution :math:`P_{X, Y}`. 

Given some target quantile :math:`\alpha` or associated target coverage level :math:`1-\alpha`,
we aim at constructing a set of possible labels :math:`\hat{T}_{n, \alpha} \in {1, ..., K}`
for a new feature vector :math:`X_{n+1}` such that 

.. math:: 
    P \{Y_{n+1} \in \hat{T}_{n, \alpha}(X_{n+1}) \} \geq 1 - \alpha


1. Split-conformal method
-------------------------

- In order to estimate prediction sets, one needs to "calibrate" so-called conformity scores
  on a given calibration set. The alpha-quantile of these conformity scores is then estimated
  and compared with the conformity scores of new test points output by the base model to assess
  whether a label must be included in the prediction set

- The split-conformal methodology can be summarized in the scheme below : 
    - The training set is first split into a training set and a calibration set
    - The training set is used for training the model
    - The calibration set is only used for getting distribution of conformity scores output by
      the model trained only on the training set. 


2. The "score" method
---------------------

3. The "cumulated score" method
-------------------------------

4. The cross-conformal method
-----------------------------



TO BE CONTINUED

[2] Mauricio Sadinle, Jing Lei, & Larry Wasserman.
"Least Ambiguous Set-Valued Classifiers With Bounded Error Levels."
Journal of the American Statistical Association, 114:525, 223-234, 2019.

[3] Yaniv Romano, Matteo Sesia and Emmanuel J. Candès.
"Classification with Valid and Adaptive Coverage."
NeurIPS 202 (spotlight), 2020.

[4] Anastasios Nikolas Angelopoulos, Stephen Bates, Michael Jordan and Jitendra Malik.
"Uncertainty Sets for Image Classifiers using Conformal Prediction."
International Conference on Learning Representations 2021.