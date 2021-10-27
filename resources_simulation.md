# Simulations for variable selection

## Independent-variable differential-mean 

"For dataset 1, we simulated a
10,000 × 784 matrix, each element of which followed a uniform dis-
tribution on (0,1), and treated its rows and columns as samples and
variables respectively. The samples were randomly assigned into
two classes of equal size, and p ′ = 64 variables were chosen at ran-
dom with their values in one class being shifted by a small amount
between 0.1 and 0.3. In this way, the 784 variables were indepen-
dent from each other, and the 64 chosen variables were significant
because each of them had different mean values in the two classes" (Sun & Li. *Nat Mach Int*, 2021). 

## Correlated variables

"As the pixel value of image
data usually highly depends on the values of surrounding pixels,
here we used all images of digit 0 in the MNIST data 23 and randomly
assigned them into two classes. Then we picked p ′ = 64 variables
and shifted their mean values in one class." (Sun & Li. *Nat Mach Int*, 2021). 

## Differential variances

"the only difference
between the two classes was that 64 out of 784 variables were made
to be ‘noisier’ with their standard deviations being inflated from
0.29 to 0.95" (Sun & Li. *Nat Mach Int*, 2021).

## Regression

"Dataset 4 was a regression data-
set. It was a 10,000 × 784 matrix whose elements were uniformly
distributed on (−1,1), and 64 of the 784 variables were randomly
chosen as significant variables. The response variable depended on
the main effects and interactions of the significant variables as well
as their nonlinear transformations." (Sun & Li. *Nat Mach Int*, 2021).
