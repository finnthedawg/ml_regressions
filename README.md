#  ml_regressions

---

## Experiments in linear, logistic, polynomial regression and regularization

---

## Dataset 1.

A visialization of the data provided:

<p align="center">
  <img width="300"  src="/figures/figureinitial.png">
</p>

```
iterations = 100
learn_rate = 0.01
```
With the above parameters and using gradient descent of the MeanSquareError cost function. We obtained the following (log) cost curve that found the minima quickly. Resulting in the following output line

<p align="center">
  <img width="300"  src="/figures/firstcost.png">
  <img width="300"  src="/figures/firstboundary.png">
</p>

## Dataset 2.

A visialization of the data provided:

<p align="left">
  <img width="300"  src="/figures/figureinitial_2.png">
  <img width="300"  src="/figures/figureinitial_3.png">
</p>

```
iterations = 500000
learn_rate = 0.0011
```
A logistic linear model was selected because the predictions to be generated should be discreet. I used the above hyper-parameters and obtained the following cost curve and decision boundary

<p align="center">
  <img width="300"  src="/figures/firstcost_2.png">
  <img width="300"  src="/figures/firstresult_2.png">
</p>

However, as the data polynomial, I expanded the input feature-set to include 5 degrees. I also normalzied the input space to the standard deviation of the input. This, enabled us to have lower iterations and a higher training rate:

```
iterations = 50000
learn_rate = 0.1
```
Todo: Fix the shifting of prediction.
<p align="center">
  <img width="300"  src="/figures/firstcost_3.png">
  <img width="300"  src="/figures/firstresult_3.png">
</p>
