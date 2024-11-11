# SIR_and_SEIR_models
**Question Number 1**

Elisa Rosnes
erosnes@emory.edu

## Part A-C SIR Model
Looking at figure 1 we can see that infection peak occurs at day 40. The peak of infection correlates with the the intersection of susceptible and recovered. As less people are susceptible and more are recovering, the infected rate will level off and then decline. 

Basic reproductive number (R0) has a large impact on the pandemic spread. It is calculated by R0 = transmission rate divided by recovery rate. In our this case R0 = 0.0003 / 0.1 which is 0.003. The smaller R0 is slower the infection will spread, and it will be easier to contain because it represents a smaller transmission rate (B) or a faster recovery rate (G). However, if for example the basic reproductive number was .03 we would have a much faster spread because either the recovery rate is slower or the transmission rate is faster both resulting in a less controlable spread. 

General pandemic dynamics: You will always see the susceptible fall off at the beginning as infection increases, there will be a point in which people recovering causes the infection rate to level off, the susceptible will continue to drop as recovered continues to rise. The peak of infection will also always correlate with the intersection of susceptible and recovered. 

## Part D: SEIR Model with Births and Deaths
The SEIR model is a more accurate representation of pandemic spread than the SIR model. It takes into account those who have been exposed, birth and death rates, and an incubation rate between exposure and infected. With these additional features we can map additional spikes in the infectious where the SIR model could not see. Depending on the R0 number, we might see one or more additional peaks of infection, these rates effect the frequency and magnitude of the infection waves. Because of these parameters we do have a higher computational cost but I believe it is often worth the accurate results and trend forecasting specifically in diseases that have an incubation period.

**Observations:**
- The peak of the number of infected correlates to the intersection between susceptible (S) and recovered (R). 

- I also notice that the second smaller wave of infected is preceded by a local maximum of susceptible and a local minimum of recovered. This makes intuitive sense because the more people that are susceptible, the more possible exposures and resulting infected.

- The exposed peak can predict the infected peak as it precedes it by a a few days. 

Including the birth/death rates effects the pandemic dynamics because it brings new people into the susceptible pool that were previously unaccounted for (because the rate is positive).

## Part E: Sensitivity Analysis 
As expected, the sensitivity has significant impact on the timing and magnitude of infection. To show drastic range I chose three sets of gamma (G) and beta (B) values as noted in figure 4: (0.05, 0.0001), (0.05, 0.0005), (0.2, 0.0001). A larger transmission rate keeping the recovery rate the same (larger R0 value) had a tremendous impact on the magnitude of infected and how quickly that peak occurs. Thinking about spread management and public health interventions, greater more drastic measures would need to be taken with a much quicker response time than if the R0 is lower. 

## Other thoughts/Improvements
I'm curious how significant population density is on the results of these models. I would think it could actually just be accounted for by tuning the infectious rate to account for a higher exposure to people. 

I'm not sure how beta and gamma are found but accuracy in that measurement or calculation is crucial. It seems like you could use machine learning to estimate these constants given real world data. On that thought of machine learning, we talked about deterministic and stochastic modeling and this seems like an area that adding in real-world randomness and variability could give you a range of outcomes instead of maybe a misleading deterministic model. It could be beneficial to see worst case/best case.

