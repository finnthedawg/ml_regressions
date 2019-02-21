#  ml_regressions

### Experiments in linear, logistic, polynomial regression and regularization

To execute the project, simply
```
git clone
jupyter notebook Linear regression.ipynb
```

## Dataset 1.

A visialization of the data provided:

<p align="center">
  <img width="350"  src="/figures/Figureinitial.png">
</p>

```
iterations = 100
learn_rate = 0.01
```
With the above parameters and using gradient descent of the MeanSquareError cost function. We obtained the following (log) cost curve that found the minima quickly. Resulting in the following output line

<p align="center">
  <img width="350"  src="/figures/firstcost.png">
  <img width="350"  src="/figures/firstboundary.png">
</p>

## Dataset 2.

A visialization of the data provided:

<p align="center">
  <img width="350"  src="/figures/figureinitial_2.png">
  <img width="350"  src="/figures/figureinitial_3.png">
</p>

```
iterations = 500000
learn_rate = 0.0011
```
A logistic linear model was selected because the predictions to be generated should be discreet.
<p align="center">
  <img width="250"  src="/figures/logistic.png">
</p>
I used the above hyper-parameters and obtained the following cost curve and decision boundary

<p align="center">
  <img width="350"  src="/figures/firstcost_2.png">
  <img width="350"  src="/figures/firstresult_2.png">
</p>

However, as the data polynomial, I expanded the input feature-set to include 5 degrees. I also normalzied the input space to the standard deviation of the input. This, enabled us to have lower iterations and a higher training rate:

```
iterations = 50000
learn_rate = 0.1
```
Todo: Fix the shifting of prediction.
<p align="center">
  <img width="350"  src="/figures/firstcost_3.png">
  <img width="350"  src="/figures/firstresult_3.png">
</p>

## Dataset 3.

A visialization of the data provided:

<p align="center">
  <img width="350"  src="/figures/figureinitial_4.png">
  <img width="350"  src="/figures/figureinitial_5.png">
</p>

A polynomial logistic linear regression model was created due to the polynomial and discreet nature of the data.

```
poly_count = 10
iterations = 100000
learn_rate = 5
reg_lambda = 0
```

**Note:** The above hyper-parameters are higher than comparitive models on the same dataset because normalization was not applied in this case. By not normalizing, we used higher parameters to have similar results.

The results and cost curve:

<p align="center">
  <img width="350"  src="/figures/firstcost_4.png">
  <img width="350"  src="/figures/firstresult_4.png">
</p>

We observed that there was a lot of overfitting. So we introduced L2 regularization to our model. The following cross entropy cost equation was used.
<p align="center">
  <img width="600"  src="/figures/crossentropy.png">
</p>

```
poly_count = 10
iterations = 100000
learn_rate = 5
reg_lambda = 0.5
```

<p align="center">
  <img width="350"  src="/figures/firstcost_5.png">
  <img width="350"  src="/figures/firstresult_5.png">
</p>
