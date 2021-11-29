# Diabetes mellitus Risk Prediction
Profiles of healthy people and diabetic people were analyzed and used to build a predictive model to gauge the diabetes risk index of an untested person.

The [dataset](https://www.kaggle.com/johndasilva/diabetes/downloads/diabetes.zip/1) we worked with was acquired from a hospital in Frankfurt, Germany. It contains a profile of health indicators such as BMI, Age, and Blood Glucose levels of individuals with and without Diabetes.

## How to Run
Download the file and run on Jupyter Notebook.

At the bottom of the file, you'll be required to enter your health indicators, such as your BMI, Blood Glucose levels, Age, etc. The predictive model will return a Diabetes Risk Index and give a short health recommendation based on that.

## Project Goal

The prevalence of Diabetes in Singapore (10.5%) is not only higher than the world average (8.8%), but is also [ever increasing](https://www.healthhub.sg/a-z/diseases-and-conditions/626/diabetes). 

According to the World Health Organization (WHO), apart from prevention, [early diagnosis is one of the most effective ways](https://www.who.int/en/news-room/fact-sheets/detail/diabetes) to minimize the burden caused by diabetes. Our objective here was therefore to train a predictive model using the available data to learn what the profile of a person afflicted with Diabetes looks like. This model would then receive the profile of an untested individual, and based on that person's health indicators, measure the similarity of their profile against that of a person with diabetes, and assign that person a value that represents their predicted risk of having Diabetes.

By better educating individuals on their diabetes risk factor, the disease can be diagnosed and tackled earlier. The predictive model serves as a means to impart (possibly life-saving) health literacy to its users.

## Possible improvements

Some future improvements to improve our model's effectiveness could be:
- Use an error metric other than accuracy score, like f1 score or precision.
- Use domain knowledge (acquired from a Doctor or another more qualified person) to make better choices about feature engineering/selection. The weightage of each health indicator could also be tuned better using domain knowledge.
- Doing the prediction with algorithms like Neural Networks instead of Logistic Regression. 
- Using a larger data-set - ideally one from Singapore.
- Think of a different way to convert predicted Diabetes Probability into Risk Index.
- Right now, blood glucose levels might not be properly standardized. We don't know if they represent the average blood glucose level over a week, or whether it was taken at a single point randomly in the day. In the latter case, it would be greatly susceptible to the time of the day it was taken, so factors like whether the person just had a meal might change it substantially. 
- Deploy the model online as a Web App, possibly using Flask, or RStudios/Shiny. 

### Images

![Prediction Example](https://i.gyazo.com/40c209e5563e2450e0c4150269405c9f.png)


## Future Expansions + Scope

### Incorporation of Sickness Diary for the Web-App
**In the spirit of preventiveness, a program such as this could be incorporated into an App along with a sickness diary, that also tracked other illnesses**, where the patient can enter info on when they were sick, as well details of the sickness and such. For instance if they had a fever, the app would also prompt them to record the temperature of their fever, and also keep track of how many days until the fever subsided, etc. The app could also track their medications taken.

**In this way, a log would be recorded of all their illnesses.**

This would reap the following additional benefits:
- We would use that data to give them **summary information about their health** in the past 6 months or so, and **if worrying trends were spotted**, that could be highlighted to them right away, similar to the way the diabetes risk index program currently works. 
- We would have the ability to **spot trends in illnesses by locale**. For instance let’s say we notice in the west, on a particular week, there’s a slight increase in ours users reporting having a cough/fever, that’s something we would be able to alert our users to. 
- **Trends could be observed between medications taken, and how long the illness took to subside**. 

### Long-term Vision
The long term vision of this goal would be to have a system in place where **a user could look back on their last 10 years of health history, and view summary information** like what was their highest peak fever in a certain year, what was the longest period of time in those 10 years that they went without having any illness (which might indicate to them that they were living a healthier lifestyle in that time), what period of time they had the most number of illnesses in, the kind of medications they took most frequently, etc.

The following benefits would also be likely:
- For medical professionals, this data could also improve invaluable in understanding patient profiles that make them more susceptible to various illnesses later in life. 
- With enough data collected, Data Scientists could use this information to implement predictive algorithms like Neural Networks to predict the occurrence and the course of an illness ahead of time.
