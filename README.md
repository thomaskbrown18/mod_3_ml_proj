
# Module 3 - Machine Learning Project:

The purpose of this project is to examine data from one of Austin's largest animal shelters and build a machine learning model to predict outcomes of animals as they come in and are processed in the system.  An efficient and intelligent model can help "manage the inventory" of the shelter and get animals adopted more quickly or returned to their owners more quickly when applicable.  <br><br>
The outcomes are listed below:
- Transfer           
- Adoption           
- Euthanasia        
- Return to Owner     
- Died                 
- Rto-Adopt
- Missing
- Disposal  <br>

We'll explore these outcomes (as well as the sub categories) in the EDA phase, but with an effective model, we can run the shelter more efficiently leading to happier animals and shelter employees!

Stakeholders: The stakeholders for this project are both the Austin Animal Center and shelters everywhere. The goal is to bring focus to animals that need to be returned to their owners, and the outcome of this project, the algorithm, can likely be adapted to shelters elsewhere.

## Objectives:

Goal: Maximum recall when it comes to the 'return to owner' outcome. We want to be certain that we are giving maximum exposure to pets that need to be returned to their families. It is not as crucial to be sure we're making the adoption/transfer process more efficient, though the more adoptions the better!

Success Criteria: 
- Easy to understand/use machine learning model
- Easy to implement algorithm
- High recall when it comes to pets that can be returned to families

## Data:

Data Source: https://www.kaggle.com/aaronschlegel/austin-animal-center-shelter-intakes-and-outcomes?select=aac_intakes_outcomes.csv

The data for this project has been generously provided by the city of Austin in their initiative for open data sources.  The data consists of roughly 80,000 rows where each row displays a different outcome of a given animal in a shelter.  For example, a row might have the data for a month old kitten, domestic short hair breed, that was taken in off the street in an injured condition and adopted a month later.  Each line tells the story of a different dog or cat's journey through the shelter.  
<br><br>
There are instances of animals getting euthanized, but as this is a no-kill shelter, I filtered these outcomes out of the data set.  When animals are euthanized at this shelter, it is because they are badly sick or injured.  This is not a call that a machine learning algorithm can make from just a line of data.


## Modeling:

For this project I built a few different models, but the ones that stood out were Random Forest due to ease of understanding and speed compared to some other models and XG Boost due to a slight increase in accuracy.  I tuned both models using number of trees, learning rate, max depth, and a few other hyperparameters.  At the end of the day, I was able to acheive roughly 80% accuracy overall for this ternary classification problem.


## Model Evaluation:

Here are the confusion matrix plots for the Random Forest and XG Boost models:


## Conclusion: 

This exercise in model building has been quite informative.  While pets returned to owners are the smallest of the main groups, it's crucial they get the attention they need instead of being transfered out or adopted to another family.<br><br>

Pets that are the most likely to have their families looking for them should be put front and center on the website so families can find them easily.  Pets likely to be adopted should be a close second.  On top of that, we can improve data collection in the future to improve the model.  There are a few major areas that could help:

- Change color upon intake to one of 15 or so values instead of an arbitrarily chosen color.  This has resulted in over 500 different colors recorded in the dataset.
- Change location data to longitude and latitude data.  This makes it much easier to compare locations.  It can also help when implementing maps on the site.
- Change breeds to a more standardized list as well.

Overall, though, this model should help the vast majority of pets find their way to owners.  With some work on the website and internal database applications, we can set up a system to help animals find their homes!

Thanks for reading,

-Thomas Brown