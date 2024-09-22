# Simple Linear Regression
$$Y\approx\beta_0+\beta_1X$$
$\approx$: is approximately modeled as  
$Y$: quantitiative response  
$X$: predictor variable  

$$\hat y = \hat\beta_0+\hat\beta_1x$$
$\beta_0$, $\beta_1$: model coefficients/parameters  
$\beta_0$: intercept  
$\beta_1$: slope  
## Estimating the Coefficients
$(x_1,y_1), (x_2,y_2), \dots, (x_n,y_n)$: $n$ observation pairs, which consists of a measurement of $X$ and a measurement of $Y$  
$\hat y_i= \hat\beta_0+\hat\beta_1x_i$: the *lease square line*, the prediction for $Y$ based on the $i$th value of $x$  
$e_i = y_i - \hat y_i$: the $i$th residual (observed_value - predicted_response_value)  
*residual sum of squares*: $\text{RSS} = e_1^2+e_2^2+\cdots+e_n^2$  
*least square approach*: used to choose $\hat\beta_0$ and $\hat\beta_1$ to minimize the $\text{RSS}$
$\hat\beta_1=\frac{\sum_{i=1}^n(x_i-\bar x)(y_1-\bar y)}{\sum_{i=1}^nx_i-\bar x}$  
$\hat\beta_0=\bar y-\hat\beta_1\bar x$  
$\bar y\equiv\frac{1}{n}\sum_{i=1}^ny_i$  (sample means)  
$\bar x\equiv\frac{1}{n}\sum_{i=1}^nx_i$  (sample means)  
## Assessing the Accuracy of the Coefficient Estimates
*true* relationship between $X$ and $Y$: $Y=\beta_0 +\beta_1X + \epsilon$ (the *population regression line*, best linear approximation to the true relationship between $X$ and $Y$)  
$\mu$: the population mean of a random variable $Y$  
Unbiased estimator, unbiasedness: The average of $\hat\beta_0$ and $\hat\beta_1$ gained from large number of data sets will be equal to $\beta_0$ and $\beta_1$; But a single estimate may be a substantial underestimate or overestimate.  

How far will $\hat\mu$ be from real?  
-> Standard error of $\hat\mu$, tells about the average amount $\hat\mu$ differs from the actual value of $\mu$: $\text{Var}(\hat\mu)=\text{SE}(\hat\mu)^2=\frac{\sigma^2}{n}$  
    $\sigma$: the standard deviation of each of the realization $y_i$ of $Y$  

How close $\hat\beta_0$ and $\hat\beta_1$ to the real value?  
$\text{SE}(\hat\beta_0)^2=\sigma^2[\frac{1}{n}=\frac{{\bar x}^2}{\sum_{i=1}^n}(x_i-\bar x)^2]$  
$\text{SE}(\hat\beta_1)^2=\frac{\sigma^2}{\sum_{i=1}^n(x_1-\bar x)^2}$  
    $\sigma^2=\text{Var}(\epsilon)$  
    Assumption: errors $\epsilon_i$ for each observation have common variance $\sigma^2$ and are uncorrelated.

In general, $\sigma^2$ is not known, but can be estimated. -> *residual standard error* $\text{RSE}=\sqrt{\frac{\text{RSS}}{n-2}}$  

**Confidence Interval**: a range of values such that with 95% probability, the range will contain the true unknown value of the parameter.  
$\beta_1$: $\hat\beta_1 \pm2\cdot\text{SE}(\beta_1)$ or $[\hat\beta_1-2\cdot\text{SE}(\hat\beta_1),\hat\beta_1+2\cdot\text{SE}(\hat\beta_1)]$  
$\beta_0$: $\hat\beta_0\pm2\cdot\text{SE}(\beta_0)$ or ...  

**Hypothesis Test**:  
$H_0$: There is no relationship between $X$ and $Y$. (*null hypothesis*)  
$H_\alpha$: There is some relationship between $X$ and $Y$. (*alternative hypothesis*)  
$H_0$: $\beta_1=0$  
$H_\alpha$: $\beta_1\ne0$  

*$t$-statistic*: $t=\frac{\hat\beta-\beta_0}{\text{SE}(\hat\beta)}=\frac{\hat\beta_1-0}{\text{SE}(\hat\beta_1)}$  
*$p$-value* (probability of observing any number $\ge |t|$ in absolute value, assuming $\beta_1=0$): small $p$-value indicates association between predictor and response, when $p$-value is small enough($<0.05$), reject the null hypothesis in favour of the alternative hypothesis.
## Assessing the Accuracy of the Model
To what extent the model fits the data? -> $\text{RSE}$, $R^2$ statistic

