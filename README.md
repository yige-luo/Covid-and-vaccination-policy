# STA237A final project

As the Covid-19 crisis continues, it remains a critical task for government across the world on how to respond to such public health crisis. Protective measurements such as Covid  vaccinations are usually helpful at the individual level, yet it is not always clear at the government level on what actions to take and when to take them. In many places of the US, for example, people are reported to spent hours in the vaccination queues soon after the vaccination requirement came into effect, which increased the physical contact and therefore could work against the policy's purpose in slowing the spread of Covid.

In this project, we are planning to assess the effect of vaccination policy on the spread of Covid, and determine if policy effectiveness vary across countries. The vaccination policy is coded as dummies, with increasing stringencies ranging from no-policies to all group. The response variable is a time series of Covid growth rate, measured by # of new cases per million from Jan. 2021 to Sep. 2021 across a few selected countries. To examine the association between of vaccination policy and Covid growth, we first remove the confounding effect of Covid testing rate, and then 1) build ARIMA model as the null model, 2) include the vaccination policy in the ARIMAX models (a.k.a. time series regression models) and 3) examine the gain (if any) of variance explained by introducing the vaccination policy. Finally, we use the gain in variance explained as a proxy to evaluate the policy effectiveness in that country and compare it across all countries in an ANOVA model. 

The performance of ARIMA and ARIMAX will be examined by internal and external validation. Note that for both models, we used a subset of historical data instead of the full range data (Jan 2020 - Nov 2021). This allows us to evaluate the model external prediction accuracies by comparing the model "forecasts" and the realized data in Oct. 2021, where many other potentially contributing factors such as face covering, travel restrictions, weather conditions are also at play.

The significance of our aims lie in our abilities to make suggestions to policy makers in countries where they have not publicized vaccination guidelines. If the effectiveness of vaccination policy (measured by the gain in variance explained) is uniformly strong, there are good reasons to believe the policy is generaly helpful and the government should follow the existing practices. On the other hand, if there substantial variations exist in the policy effectiveness, the government should probably think twice before leap, and hopefully incorporate its nation-specific reality (such as the capacity of vaccine production, amount of vaccine import) during decision making.
 
Data source: [Our World in Data](https://ourworldindata.org/), where the dynamic of Covid growth worldwide and government policy responses to Covid are well curated. 

To keep track of our latest project progress, check the [project report](https://docs.google.com/document/d/1mLVGCqgoFnD9lBLHMLsJCH9e5bdnuzaUxqxj2XuNoJ4/edit?usp=sharing) and [presentation slides](https://docs.google.com/presentation/d/1vkR1hbfJ4n93x9V6-DSgULi_Gs2n-iIjJObrVRvfapo/edit?usp=sharing).

# Reference
+ Hossain, Md. S., Ahmed, S., & Uddin, Md. J. (2021). Impact of weather on COVID-19 transmission in south Asian countries: An application of the ARIMAX model. The Science of the Total Environment, 761, 143315. https://doi.org/10.1016/j.scitotenv.2020.143315
+ Edward E. Time series models with covariates, and a case study of polio. 2016 April 14. Retrieved November 6, 2021, from https://ionides.github.io/531w16/notes18/notes18.html
+ Hyndman, R. J. (2010, October 4). The ARIMAX model muddle | R-bloggers. Retrieved November 6, 2021, from https://www.r-bloggers.com/2010/10/the-arimax-model-muddle
