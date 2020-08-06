## SIMULATION PROJECT - R PROGRAMMING

## Simulation Study 1, Significance of Regression

In this simulation study we will investigate the significance of regression test. We will simulate from two different models using the data found in study_1.csv file:

The “significant” model 
Yi=β0+β1xi1+β2xi2+β3xi3+ϵi
where ϵi ~ N(0,σ2) and β0 =3, β1 =1, β2 =1, β3 =1.

The “non-significant” model
Yi=β0+β1xi1+β2xi2+β3xi3+ϵi
where ϵi
 ~ N(0,σ2
) and β0 =3, β1 =0, β2 =0, β3 =0.

For both, we will consider a sample size of 25 (n = 25) and three possible levels of noise. That is, three values of σ
 i.e., σ ∈ (1,5,10)

Then for each of the three values of σ, for calculate the following for both models.

A. The Fstatistic for the significance of regression test
B. The p-value for the significance of regression test
C. R2

For each model-σ combination we will use 2500 simulations. Then for each simulation, we will fit a regression model.

## Simulation Study 2, Using RMSE for Selection

Using the data found in study_2.csv, We will simulate from the below model

Yi=β0+β1xi1+β2xi2+β3xi3+β3xi4+β3xi5+β3xi6+ϵi
where ϵi ~ N(0,σ2) and β0 =0, β1 =5, β2 =-4, β3 =1.6, β1 =-1.1, β2 =0.7, β3 =0.3.

We will consider a sample size of 500 and three possible levels of noise. That is, three values of σ i.e., n=500 and σ ∈ (1,2,4).

We simulate the data by randomly splitting the data into train and test sets of equal sizes (250 observations for training, 250 observations for testing).For each simulation, we fit the nine models, with forms as shown below:

y ~ x1

y ~ x1 + x2

y ~ x1 + x2 + x3

y ~ x1 + x2 + x3 + x4

y ~ x1 + x2 + x3 + x4 + x5

y ~ x1 + x2 + x3 + x4 + x5 + x6

y ~ x1 + x2 + x3 + x4 + x5 + x6 + x7

y ~ x1 + x2 + x3 + x4 + x5 + x6 + x7 + x8

y ~ x1 + x2 + x3 + x4 + x5 + x6 + x7 + x8 + x9

For each model and for each of the level of noise, we simulate 1000 times and calculate the Train and Test RMSE to identify the best model.

## Simulation Study 3: Power

we will investigate the power of the significance of regression test for simple linear regression.

H0:β1=0 vs H1:β1≠0

Power is the probability of rejecting the null hypothesis when the null is not true, that is, the alternative is true and β1 is non-zero.Many things affect the power of a test. In this case, some of those are:

Sample Size, n
Signal Strength, β1
Noise Level, σ
Significance Level, α
In this study, we’ll investigate the first three. To do so we will simulate from the model

Yi=β0+β1xi+ei

We will then consider different signals, noises, and sample sizes:

β1 ∈ (−2,−1.9,−1.8,…,−0.1,0,0.1,0.2,0.3,…1.9,2)

σ ∈ (1,2,4)

n ∈ (10,20,30)

We will hold the significance level constant at α=0.05 . 
