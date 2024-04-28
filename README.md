# InternetBuzzBoxOffice
Analysis of the impact of 'Internet buzz' on movie box office revenues, using data from 62 wide-release movies.

1. Project Overview:

This project is based on the undergraduate honors thesis by Versaci (2009) that investigated the concept of "Internet buzz variables". The goal is to determine whether these buzz variables offer any additional predictive value for a movie's box office revenues, beyond traditional movie characteristics such as genre, actors, and budget.

2. Dataset:

The dataset used for this project, boxOffice.csv, contains data for 62 movies that were widely released between November 7, 2008, and April 3, 2009.

The variables in the dataset are as follows: (here you can add your table or list of variable descriptions)

3. Analysis Approach:

The initial analysis will be conducted without considering the "buzz" variables (addict, cmngsoon, fandango, and cntwait3). Further analysis strategies and steps will be determined based on these initial findings.

## Variable Descriptions

| Variable  | Description |
| --------- | ----------- |
| box       | Domestic opening weekend box office revenues ($) |
| G         | Binary variable indicating if the MPAA rating code is G (0 if not) |
| PG        | Binary variable indicating if the MPAA rating code is PG (0 if not) |
| PG13      | Binary variable indicating if the MPAA rating code is PG-13 (0 if not) |
| budget    | Production budget (in millions of $) |
| starpowr  | Star power rating based on the Forbes 2009 Star Currency list (range: 0 to 10) |
| sequel    | Binary variable (1 → sequel; 0 → if not) |
| action    | Binary variable indicating if the movie genre is action (0 if not) |
| comedy    | Binary variable indicating if the movie genre is comedy (0 if not) |
| animated  | Binary variable indicating if the movie genre is animated (0 if not) |
| horror    | Binary variable indicating if the movie genre is horror (0 if not) |
| addict    | Number of trailer views at traileraddict.com |
| cmngsoon  | Number of message board comments at comingsoon.net |
| fandango  | Sum of “can’t wait” and “don’t care” votes at fandango.com |
| cntwait3  | Percent of “can’t wait” votes at fandango.com |

## Key Takeaways and Surprises

### Surprising Observations:
- During the PCA for dimensionality reduction, I found that the first four principal components explained over 90% of the variance in the data. However, as more principal components were added to the model, the adjusted R-squared improved up to a certain point (model 10) but then decreased for model 11. This was surprising considering that the first two principal components alone explained 80% of the variance as compared to the first four, which explained more than 90%. 
- This experience taught me that I can't solely rely on the rule of thumb and select principal components based on the cumulative variance explained by them. By building multiple models, I was able to narrow down to a more effective model.

### Managerial Takeaways:
- The data from 'addict', 'cmngsoon', 'fandango', 'cntwait3' provided additional predictive information for box office revenues, thus these "buzz" variables are significant in predicting box office revenues. This suggests that generating buzz on these platforms could potentially boost box office revenues.
- While the PCA did not provide an exact recipe for the combination of the four buzz variables, 'starpowr', and 'budget', it did imply that these variables play a substantial role in predicting box office revenue.
- 'PG', 'action', 'animated', and 'comedy' turned out to be significant variables in the best-performing model.
- There is room for improvement in this model. More data points and features are required for better box office revenue prediction.
- Possible additional features for improvement could include region-specific movie distribution data, marketing data, script analysis, as well as factors such as director power, technician power, and original sound score.
