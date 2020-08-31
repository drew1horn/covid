# COVID-19

A Coronovirus SIR model on a continuous space.

* Forked from Tom's https://github.com/trobey/covid
* Just cloned Tom's repo
** Because I wasn't ready to think about using git in a shared environment
** I just wanted to start working on my version now!
** I plan on merging back into Tom's repo

* Backporting my latest 

## Parameters
### Prefork - Tom's
* Population - Number of people (density) with one asymptomatic infected person.
* Imperial College model - Agents move through home, work and community spaces like the Imperial College model.  If this is turned off then agents move through simple diffusion.
* Asymptomatic - Percentage of infected people that are asymptomatic.  Asymptomatic people transmit the virus for 42 time steps versus 15 time steps for those that are symptomatic.
* Social Distance - Distance at which neighboring susceptible agents can become infected.
* Mobility - The maximum distance that an agent can travel.

### Drew's
* Immune (%) - Percentage of Population Immune to COVID-19, either naturally or as a result of vacines.
* Morality Over Capacity (%) - Mortality rate when healthcare syste is operating beyond its capacity.
* Capacity (%) - Capacity of healthcare system to treat COVID-19. For some applications absolute number instead of Percentage might be better.
* Mortality Under Capacity (%) - Mortality rate when healthcare system is operating within its capacity.

## Issues
* Mortality rate calculations are first draft many problems ago. Needs verification and calibration.
* See notes, in covid/server.py and covid/StackedChartModule.py regarding stacked charts.
* Verify Imperial College Model.
** But first, let's figure out how to split the video into three screens
** It's too hard see what's happening in ICM mode
*** Home
*** Work
*** Community
** It will be a while before I know enough to tackle this
** Need to dig deep into mesa

* Not, sure about np.array usage throughout model.
** Think it's just useless cruft from long ago
** Testing first
** Then I hope to whack it
** making the code more readable

