# Methodology
## Data Source(s)
While conducting this research and analysis, I found the file "food-world-cup-data.csv" in FiveThirtyEight. As someone that loves different types of food, this file peaked my interest and had lots of data ready to sift through and analyze.
## Data Preparation/Cleaning
For the preparation of this data, I had to look at the data source as a puzzle: many pieces and a lot to analyze. To summarize this data, a survey was conducted with 1,373 respondents ranking the cuisine of each given country. Many other factors about these respondents were taken into consideration for this survey:
- Gender
- Age
- Household Income
- Education Level
- Location/Region

These are all important factors for this analysis because:
- Different ages have different experience; someone who is older has lived more years and possibly traveled to more countries.
- If someone has a higher income, they may have more money to spend on traveling to different countries.
- Depending on region, some people may only have access to their cultures’ cuisine/cuisine of countries near them.
- If someone is significantly busy such as a college student who's still currently in school, they may not have the time to travel or try different kinds of cuisine.
- Some people are just picky and not willing to try new cuisines.

Another way I looked at this data was by taking the description of each column by doing the following code:

        import pandas as pd
        import numpy as np
        foods = pd.read_csv('food-world-cup-data.csv')
        foods['Please rate how much you like the traditional cuisine 
        of {given country}.'].describe
When using this general code and filling in a specific country from the .csv file, the code would return information such as the maximum rating, minumum rating, mean, etc. I then took the mean of each country so that I could later use that information to see which country had the highest mean rating.

For the other categories that did not include a number ranking, I performed the following code. For example of one, I did:

    foods['How much, if at all, are you interested in cuisines from different parts of the world?'].value_counts()
This code returned the number of respondents that gave each of the following responses:
- 651 respondents have some interest
- 438 respondents have a lot of interest
- 200 respondents have not much interest
- 84 respondents have no interest at all

## Assumptions
Some educated assumptions that I made from my data was that if a respondent answered "Advanced" to the question "Generally speaking, how would you rate your level of knowledge of cuisines from different parts of the world?", they were more likely to have tried more types of cuisine. In that case, those respondents were more likely to not answer "N/A" when asked to rate a specific cultures cuisine. Nevertheless, those with "advanced" palates did respond with "N/A" to some cuisines, since most people have not tried every type of cuisine listed.
## Limitations
As I stated previously in my data cleaning/preparation, there were many important factors that played into this data, with some of those being assumptions. A large limitation was that the data did not always line up with those accusations. For example, although someone has a lower household income than someone else, that doesn't necessarily mean that they've had less opportunities to try a bunch of different cuisines than someone more fortunate.