# Regression Analyses

In week 4 of the University of Michigan's Foundations of Sports Analytics: Data, Representation, and Models in Sports we explored a National Football League (NFL) dataset and practice using regression analyses to explore the impact of several external factors on game outcomes. 

For this assignment, we explored an NFL historical game result dataset. This dataset also contains basic information on NFL teams and the stadiums where the games took place. Additionally, this dataset contains game day weather information. You will test if there is home game advantage for the teams and if external factors such as stadium condition and weather have any impact of teams’ ability to score. 

## I. Import and Explore Data
1)  Import the “nfl_game.csv” data file and name the dataframe as “NFL_Game” in Jupyter Notebook.
Descriptions of selected variables
    - Unit of measurement of weather variables: 
       - temperature - degree Fahrenheit; 
       - humidity – relative percentage;
       - wind – mph
    - The variable “score” is the score earned by the team specified in the “team” variable. The variable “opponent_score” is the score earned by the team specified in the “opponent” variable.
    - The variable “score_diff” is defined as “score – opponent_score” for the given team.
    - The variable “stadium_age” is defined as the difference between the year of the season and the year the stadium opened.
    - The variable “stadium_neutral” indicates if the game was played in a third stadium, which is neither the home team’s nor the away team’s own stadium.

2)  Use the “describe” function to calculate summary statistics for the “date” variable. Use the “describe” function to calculate summary statistics for the “score” variable based on whether it is a home or an away game for the team.

3) Find the correlation efficients between the following pairs of variables:
    - “win” and “home”       
    - “score_diff” and “home”
    - “score” and “weather_temperature”
    - “score” and “weather_humidity”       
    - “score” and “weather_wind_mph”

## II. Regression Analysis 1 – Test of Home Game Advantage 
In this regression analysis, you will try to determine if playing at home gives teams any advantage in their performance.

Run the following regressions where the variable “score_diff” is the dependent variable.

Reg1_1: Include a single variable “home” as the independent variable.

Reg1_2: Include the “home,” “stadium_capacity,” “stadium_neutral” variables and the interaction between “home” and “stadium_neutral” as the independent variables.

Reg1_3: Include the “home”, “stadium_capcity,” and “stadium_neutral” variables, the interaction between “home” and “stadium_neutral,” as well as “team” and “opponent” as the independent variables.

## III. Regression Analysis 2 – Impact of Outside Factors on Scores
In this regression analysis, you will investigate if the final score earned by each team is affected by outside factors such as the size and condition of the stadium as well as weather conditions at the stadium.

Run the following regressions where the variable “score” is the dependent variable.

Reg2_1: Include “season” and “home” variables as independent variables.

Reg2_2: Include “season,” “home,” “weather_temperature,” “weather_wind_mph,” and “weather_humidity” as independent variables.

Reg2_3: Include “season,” “home,” “weather_temperature,” “weather_wind_mph,” “weather_humidity,” “stadium_capacity,” “stadium_age”, “stadium_type,” “stadium_neutral”, and the interaction between “home” and “stadium_neutral” as independent variables.     

Reg2_4: Include “season,” “home,” “weather_temperature,” “weather_wind_mph,” “weather_humidity,” “stadium_capacity,” “stadium_age”, “stadium_type,” “stadium_neutral”, and the interaction between “home” and “stadium_neutral” as independent variables. Additionally, add both “team” and “opponent” in the regression.
