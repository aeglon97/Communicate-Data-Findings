# PISA 2012 DATA EXPLORATION & VISUALIZATION
## by Marc Angelo Acebedo


## Dataset

PISA is a survey of students' skills and knowledge which takes place at the end of their compulsory education, looking at how well-prepared students are for life after school. Around 486,000 students in [65 countries](http://www.oecd.org/pisa/aboutpisa/pisa-2012-participants.htm) took part in this survey.

The full dataset can be found [here](https://s3.amazonaws.com/udacity-hosted-downloads/ud507/pisa2012.csv.zip) and the explanation for each column can be found [here](https://s3.amazonaws.com/udacity-hosted-downloads/ud507/pisadict2012.csv).

After combing through the original dataset, I decided that I needed a solid 10-15 variables to isolate for the scope of this project. My data wrangling process can be found [here](https://github.com/nihlan97/Communicate-Data-Findings/blob/master/pisa2012_wrangle.ipynb), exploration phase where I describe all features in-depth [here](https://github.com/nihlan97/Communicate-Data-Findings/blob/master/pisa2012_exploratory.html), along with the presentation [slides](https://github.com/nihlan97/Communicate-Data-Findings/blob/master/pisa2012_explanatory_slides.slides.html).


## Summary of Findings


### Univariate

***All Environment and Student Drive variables appear heavily left-skewed, with the exception of Work Ethic which has an outlier of score = 2. This indicates that of the students who answered these 2 variable groups, the averange student picked answers that were more favorable to their self-image and/or perception of the school.*** The outlier at Rating = 2 under Work Ethic is so significant that it *affects the entire distribution, making it multimodal as opposed to more or less a normal distribution without it.* 

As for mother occupation, I found that "Housewife" is the most common mother occupation at 24.1%. This is an unusual point because the difference is drastic in comparison to the second most common mother occupation, "Shop sales assistant," at 4.2%. The difference in the top 2 most common mother occupations is 19.9%. As for students who answered "Yes" or "No" to mother immigration status, the overwhelming majority answered "Yes" at 77.83%. 

### Bivariate

One of the main takeaways is that ***students with immigrant mothers tend to have more pessimistic views of themselves under student drive variables, but consistently outperform non-immigrant students by a large margin.*** This is interesting coupled with the fact that students with immigrant mothers acclimate better to their environment than students who do not come from an immigrant background.

The second main insight is that ***girls tend to have a greater work ethic than male students, but a much lower self-esteem in comparison.***

Other relationships include the fact that even though Mexico is the most frequently occurring country, it is in the bottom 15 of countries that scored the worst for math, reading, and science scores. Students whose mothers work primarily blue-collar jobs are the most likely to score the worst on math, reading, and science ***however***, they tend to score higher for work ethic. Contrarily, students with parents who work in STEM and/or other white collar jobs exclusively score the highest for math, reading, and science - this means that a student is less likely to score well on tests if their parents hold blue-collar jobs.

Additionally, Shanghai, China dominates every other country when it comes to landing the global highest math, reading, and science scores. 

### Multivariate

For this section, I wanted to explore my previous two main takeaways from in-depth.

Rather than just correlating having an immigrant mother to student drive and acculturation scores, I wanted to ***analyze how acculturation rates varied for students from immigrant backgrounds by country***. Through this exploration, I discovered that Italy and Denmark host the students who, on average, feel the most acclimated to their environment. However, the only exception where students from immigrant backgrounds scored less than non-immigrant children is Korea. This makes sense, considering that Korea is one of the most homogenous countries on Earth. 

The previous plots depicted that girls score better than boys on reading tests for all countries. However, I dove in a little deeper and ***analyzed how work ethic impacted scores for both genders.*** Despite girls having an overall higher work ethic, if a boy and girl had the same work ethic score, the boy is most certainly guaranteed to score higher for math. The contrary is true for reading scores, where girls prevail. *Perhaps this is reflective of the culture of girls being discouraged from pursuing STEM.*


## Key Insights for Presentation

For my presentation, I narrowed my focus to the following 2 approaches:

### Approach 1: Immigrant Background by Student Drive and Academic Performance
Here I examine the question of how having an immigrant mother can impact a student's self-perception, acculturation, and scoring. First I look at the distribution of students with immigrant mothers through a pie chart, correlate them to all student drive variables using box plots, then examine all math, reading, and science scores using both box plots and histograms.

### Approach 2: Gender by Student Drive and Academic Performance
After immigrant background, the exploratory phase raised many interesting questions surrounding gender. First I look at the distribution of gender, which is about evenly split, using a pie chart. Using box plots again, I then proceed to examine work ethic and self-esteem rates between boys and girls, and then look at score distribution by box plots and histograms.

Afterwards, I explore the question of **is girls' outperformance in reading scores over boys due to their higher work ethic? What about the other scores?** After using line plots to correlate work-ethic on the x-axis and math, reading, & science scores on the y-axis separately for both genders, I draw my conclusions at the end.

**To convert my Jupyter Notebook slides, navigate to the terminal and follow these steps:**
1. Navigate to `/Communicate-Data-Findings/`
2. type `jupyter nbconvert pisa2012_explanatory.ipynb --to slides --template output_toggle.tpl --post serve`

**To deal with the original dataset, download the full original PISA 2012 dataset linked above and move it to the `/data/` folder.**