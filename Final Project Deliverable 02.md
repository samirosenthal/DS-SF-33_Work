# Project Design Writeup


### Project Problem and Hypothesis
* What's the project about? What problem are you solving?  
My project will be focused on crime data. There are a few things that I want to look at. First, I want to look at general US crime data to evaluate if there are trends in crime type, or time of year, etc. Following that, I would like to do a more in-depth look at San Francisco crime data. I am hoping to be able to predict what neighborhoods are most likely to have particular types of crime at certain times of year ot times of day.
* Where does this seem to reside as a machine learning problem? Are you predicting some continuous number, or predicting a binary value?  
For the general US data, I will most likely use linear regression to look at relationships between variables. I will also use linear regression to look at likelihood of crime in different neighborhoods in San Francisco. I could also potentially look at the San Francisco as a categorical problem with an outcome of whether or not a crime will take place.
* What kind of impact do you think it could have?  
Looking at this data could be very useful for avoiding crime in certain areas. As a San Francisco resident, I will find this information very useful in deciding which areas to avoid in general or during certain times. This type of data could also be useful for police forces in knowing how many officers to have in certain areas compared to others.
* What do you think will have the most impact in predicting the value you are interested in solving for?  
I believe that location (either city or neighborhood within San Francisco) will have a large impact in terms of predicting likelihood of a crime. I also think that night may have a larger amount of crime than daytime.


### Datasets
* Description of data set available, at the field level (see table)  
I have found a few datasets that will be useful for this project:

* San Francisco Police Department Incidents

| Field | Description |
|---|---|
| IncidntNum | SF Police Incident Number |
| Category | Type of crime (Burglary, Vehicle Theft, Assault, etc.) |
| Descript | Short description of incident |
| DayOfWeek | Day of Week |
| Date | Date |
| Time | Time |
| PdDistrict | Police force District |
| Resolution | Incident Resolution |
| Address | Address |
| X | Longitude |
| Y | Latitude |
| Location | Longitude and Latitude |
| PdId | Unique Identifier for use in update and insert operations |


* FBI Crime in the US: Jan - Jun 2015 and 2016 for cities with population > 100,000

| Field | Description |
|---|---|
| Population | Population of city |
| Violent crime | # of Violent Crimes|
| Murder | # of Murders |
| Rape (revised definition) | # of Rapes (revised definition) |
| Rape (legacy definition)|  # of Rapes (legacy definition) |
| Robbery |	# of Robberies |
| Aggravated assault | # of aggravated assaults |
| Property crime | # of property crimes |
| Burglary | # of Burglaries
| Larceny-theft	| # of Larceny - thefts |
| Motor vehicle theft | # of Motor vehicle thefts |
| Arson | # of Arsons |


### Domain knowledge
* What experience do you already have around this area?  
I do not have any experience in this topic, besides being a resident of San Francisco and seeing/ hearing about crimes around the city.
* What other research efforts exist?  
There is a lot of research online modeling a large amount of different crime data. Some example are below:  
* [Linear Model of US Crime Rates from 1970](https://rstudio-pubs-static.s3.amazonaws.com/211668_aafed853c63f46dca91791bd379536e3.html)
* [Crime Rate Comparison Map](https://www.arcgis.com/home/item.html?id=8125e8f4244a47d986f4cd840824eef3)
* [Predicting And Mapping Arrest Types in San Francisco](http://minimaxir.com/2017/02/predicting-arrests/) - This one uses the same data, so it will be interesting to compare results and approaches.


### Project Concerns
* What questions do you have about your project? What are you not sure you quite yet understand? (The more honest you are about this, the easier your instructors can help).  
I am not totally sure which models I am going to use, or what will be the most useful. I think I will most likely have to play around with multiple different models to see which are the best. I also am not totally sure what will be the most useful outcome - I could predict where a crime would be based on time of day, or I could model the likelihood of crime given a neighborhood and time. All of the potential outcomes are interwoven, and I think once I start playing with the data it will be more clear.
* What are the assumptions and caveats to the problem?  
One caveat is that the data is not necessarily ideal. The crime descriptions and types are not always filled out correctly, and there are a large amount in the "Other Offenses" category.
* What is already implied about the observations in your data set? For example, if your primary data set is twitter data, it may not be representative of the whole sample (say, predicting who would win an election)  
I think the data should be representative of all crime in SF since it is coming from the police department.
* What are the risks to the project?  
    * What's the cost of your model being wrong? (What's the benefit of your model being right?)  
    It could be risky if the model predicted no crime in a certain area and someone used the model as a source of truth for which areas to go to. This could cause them to be in a bad situation. Inverseley, if the model is correct, it could save people from going to bad areas during peak crime times.
    * Is any of the data incorrect? Could it be incorrect?  
    I think that the data will all be correct since again, it is coming from the police department and the FBI.


### Outcomes
* What do you expect the output to look like?  
As I said above, I am not entirely positive what I want the outcome to be, but I think it will most likely be a prediction of which areas have the most crime during certain times, and what those peak times are.
* What does your target audience expect the output to look like?  
My target audience would be people similar to me, who would want to avoid areas that have high crime rates. I believe they would want the same output described above.
* What gain do you expect from your most important feature on its own?  
I think the most important feature will be location / district. Looking at just this feature will allow me to have a good idea of which areas I should expect to have the most crime.
* How complicated does your model have to be?  
I don't think this model needs to be very complicated. I think instead of making one complicated model, it may be more useful to make several simpler models so that I can verify my findings, as well as explore different results and models.
* How successful does your project have to be in order to be considered a "success"?  
I would like to be able to compare the model to crime data in the future and see if it predicted crimes correctly.  I am not entirely positive which metric I will use since I'm not sure which model will give me the best results.
* What will you do if the project is a bust (this happens! but it shouldn't here)?  
I will keep trying to improve! This may mean getting more data, or trying new modeling techniques.
