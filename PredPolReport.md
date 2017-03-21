
---
 \documentclass[a6paper,11pt]{memoir}
Title: 'Predictive Policing in Chicago '
author:
- Chibueze Ukachi^1^
- Alejandro Angeli Ayello^1^
include-before: ^1^ LTS2, EPFL, Switzerland
date: \today
numbersections: true
lang: en
header-includes:
- \hypersetup{colorlinks=true,allcolors=blue}

---

\begin{center}
Predictive Policing in Chicago
\end{center}



Hey man,

I found an absolutely fantastic dataset that I think you'll be interested in. It's about the crimes in Chicago from 2001 to present day

https://catalog.data.gov/dataset/crimes-2001-to-present-398a4
also, there's more detail about the dataset over here
https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-present/ijzp-q8t2/data

I did some quick preliminary pre-processing steps (we can change this later), as it is and removed NaN values aswell and that reduced how dataset from  6,288,458 to 5,604,960 which is wayyyy more than enough :D
What's awesome is that there are SOOO many questions we can answer seeing as we have the location of the crime per latitude and longitude (draw maps to highlight thing different crimes). We know the types of crimes and their neighbourhoods 
and where they were committed i.e alleyways and stuff

These are the features I think will be important, let me know if you want to add anything Else
IUCR already provides a mapping to the primary type and description (removed primary type and description)
latitude and longitude contains the geolocation data of crime (removed block, location, x,y coordinates as they say the same thing) 
we don't need ID/Case number as we are not tracking any individuals
The data is initially sorted according to when it was last updated on the site, which we don't care about. What we need is when the crime was actually committed (removed updated on) and sorted by the date that it was committed
Beat and FBI code, Ward I think just make our job complicated and more stuff to explain on a short project and I didn't think they were essential, but if you like, we can include these again.

To sum up the final columns were ['Date','IUCR','Location Description','Arrest','Domestic', 'District','Ward','Community Area','Latitude','Longitude']


-Total number of crimes per year
x axis - years
y - axis crime

-Total number of domestic & non-domestic crimes per year
x axis - years
y - axis crime


-Total number of crimes per neighbourhoods per year
x axis - years
y - axis crime


Homicides per neighbourhoods

police presence and #rate of crime 
police presence and arrest - discriminatory police, probable cause

software available for free but we ask that investment made in hotspot areas


neighbourhoods
crim
Predicting crime in Chicago

predict where crime will take place via hotspot pocling
2001 - 2013 train,
test model - 2014- 2017

Criminologists - Anthony Braga and David Weisburd  - Hotspot  policiting

Paper Policing Problem Places: Crime Hot Spots and Effective Prevention 

Idea - crime is not spread evenly throughout geographic space but rather concentrated in specific areas
(clusters of crime ) we know bars, clubs, pulic tranport hubs have high propensities for crime occurencs.

page 18



## Administration

* People involved
	* Student: Chibueze Ukachi, \texttt{chibueze.ukachi@epfl.ch}
	* Supervisor: Michaël Defferrard, \texttt{michael.defferrard@epfl.ch}
	* Professor: Pierre Vandergheynst, \texttt{pierre.vandergheynst@epfl.ch}
* Dates
	* Project duration: 20.02 - 02.06.2017 (14 weeks)
	* Delivery of the report to the lab: 09.06.2017
	* Grades to be given to the Registar's office: 23.06.2017
* Amount of work: 10 ECTS (1/3 of a semester)
* Evaluation: A Jupyter notebook which explains (i) the problem, (ii) the
  solution and, (iii) the results. Produced at the end of the project, no
  presentation required.
* Meeting of ~1h every week
* Repository: <https://lts2.epfl.ch/gitlab/michael.defferrard/fma-baselines>
	* Every file produced during the project should be in there.
* Dataset: Free Music Archive
	* Code & data: <https://github.com/mdeff/fma>
	* Paper: <https://arxiv.org/abs/1612.01840>
* The results obtained during this project will hopefully be integrated in the above paper.
	* ISMIR paper deadline: abstract April 21, full paper April 28

# References


[^fn1] Some text in which I cite an author.

[^fn2] More text. Another citation.

[^fn3] What is this? Yet *another* citation?




[^fn1]: So Chris Krycho, "Not Exactly a Millennium," chriskrycho.com, July 22,
    2015, http://www.chriskrycho.com/2015/not-exactly-a-millennium.html
    (accessed July 25, 2015), ¶6.

[^fn2]: Contra Krycho, ¶15, who has everything *quite* wrong.

[^fn3]: ibid say whattt update.


