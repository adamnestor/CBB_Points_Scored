## Statistical Analysis of Points Scored for Chicago State Men's Basketball

### Overview
  * During the 8 seasons from 2010-11 through 2017-18, the Chicago State Men's Basketball team had a record of 55-200.
  * This record ranked **last** among the 351 Division 1 Men's College Basketball programs for that time period.
  * Previous analysis has shown that *Points Scored* has a high effect on whether Chicago State wins a particular game.
  * **Therefore, this analysis aims to identify which _Game Variables_ have an effect on _Points Scored_, which ultimately may lead to more wins.**

### Tools and Resources Used  
  **Dataset** https://www.kaggle.com/andrewsundberg/college-basketball-dataset *Note: This Kaggle Dataset has since been updated with new files and data*  
  **Analytics Tool** Excel; including Data Analysis Toolpak.  
  **Analytic Methodologies** Descriptive and Inferential Statistics, Linear Regression, Multiple Linear Regression  
  **Data Visualization** Tableau  

### YouTube Project Walk-Through

### Tableau Presentation
https://public.tableau.com/shared/7KNGBC339?:display_count=y&:origin=viz_share_link

### Data Cleaning
  * Dataset originally had 90968 rows of data.
  * Initial investigation found Win/Loss record for each team of record.
  * Chicago State having the worst record; narrowed down to Chicago State games which focused in on 255 rows of data.
  * Created a season column in order to sort games by basketball season instead of calendar year.
  * Created columns for Defensive Rebounds, Unassisted FG, and 2-Pt shots made and attempted by using existing columns. 
  * Limited columns to game variables within Chicago States control (eliminated opponents game variables).

### EDA
  * I looked at the distributions of the data and the mean/median for the various numerical variables. 
  * I created a correlation heatmap to identify potential relationships in the data.

### Model Building
  * First, I identified key variables from EDA that could be tested to predict scoring more points.
  * I performed Linear Regression between *Points Scored* and each key variable.
  * **Multiple Linear Regression** - I used the key variables to predict how many points would be scored based on particular key variables.

### Key Insights
1. Increasing Points Scored is driven foremost by *Made 2-Pt FGs*. Taking high percentage *2-Pt FG Attempts* would increase Chicago State's *Points Scored*, compared to lower percentage *3-Pt FG Attempts*
![CBB_Insight_1](https://user-images.githubusercontent.com/79426455/110554337-97b6e780-8108-11eb-952c-6e992a18923b.JPG)


2. *Field Goals Made*, whether 2-Pt or 3-Pt, were driven by recording an *Assist*. Regression models retruned an increase in *Points Scored* when *Field Goals* were *Assisted* opposed to *Unassisted*.
![CBB_Insight_2](https://user-images.githubusercontent.com/79426455/110554360-a3a2a980-8108-11eb-9a77-dd97ceb3e0cb.JPG)

3. *Non-Scoring variables*, particularly defensive variables were shown to contribute to *Points Scored*. Regression models favored *Defensive Rebounds* to *Offensive Rebounds*, and suggested *Steals* as a moderate driver.
![CBB_Insight_3](https://user-images.githubusercontent.com/79426455/110554375-adc4a800-8108-11eb-8eef-09211dd93b8c.JPG)
