# **Project Name: Predicting NBA Player Salary**


**Group Name: CoolPython**

**Group Members: Ayushmaan Kumar, Ankit Yadav, Yining Li, Chenjian Yang**

**Section 2**


## **Background and Purpose of the Project:**

The National Basketball Association (NBA) is a men’s professional basketball league in North America. Player salaries are affected by tons of factors, such as their age, position, experience, performance as reflected by various basic and advanced game statistics, their business value in terms of their outside income and fan base across the world and income outside the court. 
    
We are curious about how much each of the performance related factors contribute to player's current salaries. For example, does per game assists explain salaries to a certain extent? This project uses Python to analyze the relationship between salaries and the factors mentioned above. Specifically the model takes individual players’ current year statistics as inputs and returns their predicted salaries. We are hopeful that our model would be of referential value to the general managers and individual players and their agents in negotiating the contracts.
    
In addition, we also wanted to use statistical scores to evaluate the extent to which a player improved compared to previous year. Hypothetically, players with higher scores should receive a larger salary increase in percentage.  

## **Methodology and Models:**
    
To predict player salaries, we implemented the following four models:
 
1. Linear regression: 
    
    Multiple variable linear regression is the most natural first choice. Below is the regression specification:
    
    S(t) = a*X(t) + e 
    
    where S(t) represents current salaries, X(t) is a vector capturing performance related variables. 
    
2. Ridge regression:
    
    Ridge regression imposes a penalty on the size of the coefficients to reduce the variance of the estimates. Ridge regression works best in situations where the OLS estimates have high variances, which apply to our dataset.
    
3. Lasso regression:
    
    Different from Ridge regression, Lasso regression performs variable selections. The revised penalty allows coefficients to shrink towards exactly zero. Hence LASSO usually results into sparse models that are easier to interpret.
    
4. Regression with signals:

    In this part, we list a series of factors and build a univariate linear regression model between salary and each factor to extract some significant factors with large absolute t-values. For each factor, if a player performs better than the past year, his score will plus 1 and vice versa.
    
We get our best results from the Lasso regression, for which we are able to predict NBA player salaries with R^2 of 0.584.
    
Along with the above signal model, we also computed statistical scores and find these players improved most compared to the previous year. Hypothetically, they should receive a larger salary increase in percentage:

Season 2017-2018: Blake Griffin, Dorian Finneysmith, Jake Layman, Malik Beasley, Malik Monk, Nik Stauskas, Zach Collins, Cody Zeller, Danny Green, Derrick Rose, Juan Hernangomez, Mike Conley, Nemanja Bjelica, Pascal Siakam, Bryn Forbes

Season 2016-2017: Bobby Portis, Bryn Forbes, Caris Levert ,David Nwaba, Davis Bertans, Delon Wright, Denzel Valentine, Derrick Favors, Devin Harris, Dwight Powell, Etwaun Moore, Fred Vanvleet, Gary Harris, Isaiah Taylor, Ish Smith

    
    
## **Installation Instructions:**

1. Clone the repository;
2. Run the code on virtual machine requires installing the following packages: Numpy, Pandas, Sklearn, Request,bs4,etc (Please find the detailed list of packages in requirement.txt file).
    

## **Description:**

1. STEP1: Download Libraries

2. STEP2: Installing Packages
    
    Libraries and packages are specified in the Installation Instructions section above and in the corresponding sections of the master file: Final_file.ipynb.
    
3. STEP3: Scraping the Data
    
    To scrap the data from https://www.basketball-reference.com, run scripts in the Section 3 Data Collection of the master file: get_player_stat.ipynb. The corresponding pkl file is: tfa_working_ver_1. 
    
    The dataset consists of per game statistics including (Games, Games Started, Minutes Played Per Game, Field Goals Per Game, ..., Points Per Game) for 449 players in season 2017 - 2018 from the following url:
    
    https://www.basketball-reference.com/leagues/NBA_2018_per_game.html    
    
4. STEP4: Data Cleaning

    In addition to existing variables, we added team winning percentage during the regular season as an extra variable. For the five positions, we created as a dummy variable to distinguish between backcourt(PG, SG) and frontcourt(C, SF, PF). We excluded any players with empty values and treated players who switched teams during the season as one single player. 
   
5. STEP5: Analysis and Modeling
    
    We conducted initial analysis on the final dataset calculating correlations between every pair of variables, and then implemented the four models introduced in the Methodology and Models section, and added corresponding visualizations.  
      
## **Run Instructions:**
     
For all statistical analysis and regression results, run the code in the master file: Final_file.ipynb, and follow the steps as specified in the description section above.
