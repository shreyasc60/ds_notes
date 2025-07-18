_________________________________________________________________________
## Required Packages
1. SimDesign

```r
install.packages("SimDesign")
library('SimDesign')
```

For this demonstration we'll use the **bias()** function to compare the forecasted temperatures with actual temperatures.

Let's us create some demo variables, and calculate the bias.

```r
actual_temps <- c(63.11, 60.6, 72.01, 80.6, 78.20)
pred_temps <- c(61.43, 62.01, 72.22, 81.3, 78.9)

bias(pred_temps, actual_temps)
```

Output:
```
[1] 0.268
```

A bias value closer to 0, or a lower bias values means that our model is accurate, and not biased. An **unbiased model should be close to zero**.

#### The bias() function

Basically the bias function finds the average amount that the actual outcome is greater than the predicted outcome