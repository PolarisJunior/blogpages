$title = Simple Linear Regression
$summary = An introduction to modelling linear relationships using simple linear regression.
$date = 1/24/2021
---

# Simple Linear Regression

Linear regression is a model for predicting the value of a dependent variable `y`, given the value of an independent variable `x`. Being a **linear** model, linear regression works best when the relationship between `x` and `y` is linear. 

## Scalar Linear Equation

Recall the basic equation for a 2-dimensional line:

\\[y = mx + b\\]

`y` is the dependent variable, also known as the response. It is the value we are trying to predict. 

`x` is the independent variable, also known as the explanatory variable. It is the input into our model. Usually it is a variable we are able to observe. We use `x` to make a prediction of what `y` is.

`m` is the coefficient, it is the value that describes by how much `y` changes as `x` changes. In calculus terms, since we know the derivative with respect to `x` is `dy/dx=m`, it is correct to describe `m` as the rate of change of `y` with respect to `x`.

`b` is the constant term, it is used to offset the value of `y` predicted. 

## Example and example of multiple variables

\\[y = m_1x_1 + m_2x_2 + b \\]

## Multiple Dependent Variables

$ax^2 + bx + c = 0$

\\(a \neq 0\\)

When \\(a \neq 0\\), there are two solutions to \\(ax^2 + bx + c = 0\\) and they are
\\[x = {-b \pm \sqrt{b^2-4ac} \over 2a}.\\]    

Given this basic equation, how can we generalize it? A two variable linear equation is generally not very useful for modelling relationships in real data. Real life is full of complexity and a dependent variable is rarely affected by only one independent variable.


\\[  y = x^T\beta + \epsilon  \\]

\\[ Y = X\beta + \epsilon \\]

\\[ \beta = (X^T X)^{-1} X^T Y \\]

