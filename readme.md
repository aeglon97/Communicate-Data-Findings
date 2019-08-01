# PISA Dataset Visualization
## by Marc Angelo Acebedo


## Dataset

PISA is a survey of students' skills and knowledge upon the end of their compulsory education, looking at how well-prepared they are for life after school. Around 510,000 students in [65 economies](http://www.oecd.org/pisa/aboutpisa/pisa-2012-participants.htm) took part in this survey.

The full dataset can be found [here](https://s3.amazonaws.com/udacity-hosted-downloads/ud507/pisa2012.csv.zip) and the explanation for each column can be found [here](https://s3.amazonaws.com/udacity-hosted-downloads/ud507/pisadict2012.csv).

The overall motivation for this project is to *explore what factors shape a student's self-esteem and academic performance*. To do this, I diverge on 2 different paths: examining both ***environmental*** and ***demographic*** variables.


## Summary of Findings


### Univariate

***All variables under Environment and Student Drive sections appear right-skewed, with the exception of Work Ethic without the outlier. This indicates that of the students who answered those questions, the majority picked answers that were more favorable to their self-image and/or perception of the school.***

**Mother Occupation** - "Housewife" is the most common occupation for a student's mother to have, out of all students who answered this question. This is an unusual point because in comparison to the 2nd most common mother occupation, "shop sales assistant," the difference in frequency is 19.9%, with 24.1% for Housewife and 4.2% for Shop sales assistant.

**Mother Immigrant** - Of all the students who answered the Mother Immigrant question, the overwhelming majority of students answered "yes" at 77.83%. This will be an interesting variable to dig more in-depth in the future exploration stages.

**Work Ethic** - The outlier at Rating = 2 is so significant that it ***affects the entire distribution***.

When including the outlier at Rating = 2, the Work Ethic kernel density curve and histogram display a severe left-skew. However, without this outlier, the distribution appears more or less normally distributed. This raises the question of: ***to include or not to include the outlier?*** I have decided that for future exploration, it would be more beneficial to examine this variable in both scenarios: with and without.


### Bivariate

- This is a key takeaway: students from immigrant families tend to have more pessimistic views of themselves under student drive variables, but consistently outperform non-immigrant students by a large margin. 

- Female students tend to have a greater work ethic than male students, but a much lower self esteem in comparison.

- Students with mothers who work as Drivers of carriages/other hard labor work are the most likely to score the worst on math, reading, and science, ***however***, they score higher for work ethic.

- Even though Mexico is the most frequently occurring country, it is in the bottom 15 of countries that scored the worst for math, reading, and science.

- Students with parents who work in STEM and/or other white collar jobs exclusively score the highest for math, reading, and science. You are less likely to score well on tests if your parents hold blue-collar jobs.

- Shanghai, China dominates by a large margin every other country when it comes to scores

- Students who come from an immigrant background acclimate better to their environment than students who are not from immigrant backgrounds.

### Multivariate

- The previous plots depicted that girls score better than boys on reading tests for all countries. However, I dove in a little deeper and ***analyzed how work ethic impacted scores for both genders.*** Despite girls having an overall higher work ethic, if a boy and girl had the same work ethic score, the boy is most certainly guaranteed to score higher for math. The contrary is true for reading scores, where girls prevail. *Perhaps this is reflective of the culture of girls being discouraged from pursuing STEM.*

- We established previously that students from immigrant backgrounds tend to acclimate better to their environment. However, we added a layer of complexity by comparing ***acclimation rates of students from immigrant backgrounds by country.*** From the above selected countries, Denmark and Italy 

- Italy and Denmark host the students from immigrant backgrounds who feel the most acclimated to their environment. However, the only exception where student from immigrant backgrounds feel less acclimated is in Korea. This makes sense, considering that Korea is one of the most homogenous countries on Earth.

- The trends are different among gender per math score. Boys tend to outperform girls on math while girls tend to outperform boys for reading. The gender gap, however, is much more varied for science scores.

## Key Insights for Presentation

> Select one or two main threads from your exploration to polish up for your presentation. Note any changes in design from your exploration step here.

- Female students tend to have a greater work ethic than male students, but a far lesser self-esteem.

- students from immigrant families tend to have more pessimistic views of themselves under student drive variables, but consistently outperform non-immigrant students by a large margin. We established previously that students from immigrant backgrounds tend to acclimate better to their environment. However, we added a layer of complexity by comparing ***acclimation rates of students from immigrant backgrounds by country.*** From the above selected countries, Denmark and Italy 

