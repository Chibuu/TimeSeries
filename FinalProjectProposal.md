---
title:  'The effect on crime of changing the number of police officers in Chicago'
author:
- Chibueze Ukachi
- Alejandro Angeli Ayello


tags: [nothing, nothingness]
...

#### Background
 Historically, the City of Chicago has had a high crime rate. One way to reduce and control crime is to increase the number of law enforcement officers patrolling around the city. The aim of this project is analyse the effect of changing the number of police officers on the daily proportion of arrests in Chicago.
The dataset contains more than six million recorded crimes committed in Chicago from 2001 to present day (minus 7 days). It was downloaded from data.cityofchicago.org[^1].
The auxiliary metadata includes a wide variety of information such as the type of crime (burglary, homicide), the place (bars, mall), communities/districts, whether an arrest was made, geolocation data e.t.c

[^1]: https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-present/ijzp-q8t2/data

#### Methodology

This project is split into five main components:

1. Pre-processing (data cleaning):
	* Restrict the time interval from 01/01/2001 to 31/12/2016.
	* Isolate the relative features of our model: Timestamp, Arrest and Beat[^fn2] and remove NaNs in either features if present.
	* Retrieve the number of police cars for each recorded crime from the Beat.
	* Perform dimensionality reduction in order to calculate the Proportion Of Arrests Per Day (PAPD) and the Number Of Police Cars Per Day (NPCPD) rather than Per Minute as in the original dataset.
![](/home/chib/Documents/25TimeSeries/TimeSeries/proposalPlot.png)

[^fn2]: http://curiouschicago.com/post/107620367089/know-your-beat-community-policing-in-chicago

2. Descriptive statistics: yearly changes in proportion of arrests, proportion of police cars present and proportion of total crimes.

3. Test for stationarity, cyclicity and analyse using time domain models such as MA, AR, ARMA models and frequency tools such as periodogram.

4. Predict the daily proportion of arrests in Chicago. The model will be trained using data from 2001 - 2011 and tested using data from 2012 to 2016.

5. Plot revelant graphs and provide an intuitive explanation of the results.


#### Hypothesis

There are four possible scenarios that could result from the relationship between PAPD and NPCPD


                     PAPD increase   PAPD decrease
-------             ---------------  -------------
    NPCPD increase        A              B
    NPCPD decrease        C              D

Table:  Problem Matrix.

Our hypothesis is that increasing NPCPD will indeed increase PAPD. This is because increasing NPCPD, will result in a higher number of patrols; therefore, increasing the chances of an arrest being made. So, even if there are a lot more crimes reported than observed by the police, the chances of making an arrest whilst on patrol are higher than that of making an arrest from a reported crime.



