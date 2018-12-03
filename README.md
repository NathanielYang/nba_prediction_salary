##Project Name: Predicting NBA Player Salary Upon Contract Expiration

##Group Name: CoolPython

##Group Members: Ayushmaan Kumar, Ankit Yadav, Yining Li, Chenjian Yang

##Section 2


######Background and Purpose of the Project:

    The National Basketball Association (NBA) is a men’s professional basketball league in North America. Player salaries are affected by tons of factors, such as their age, position, experience, performance as reflected by various basic and advanced game statistics, their business value in terms of their outside income and fan base across the world and income outside the court. 
    
    We are curious about how much each of the performance related factors contribute to player's current salaries. For example, does per game assists explain salaries to a certain extent? This project uses Python to analyze the relationship between salaris and the factors mentioned above. Specifically the model takes individual players’ current year statistics as inputs and returns their predicted salaries. We are hopeful that our model would be of referential value to the general managers and individual players and their agents in negotiating the contracts.
    
    In addition, we also wanted to use statistical scores to evaluate the extent to which a player improved compared to previous year. Hypothetically, players with higher scores should receive a larger salary increase in percentage.  

######Methodology and Models:
    
    For predict player salaries, we implemented the following three models:
 
    1. Linear regression: 
    
    Multiple variable linear regression is the most natural first choice. Below is the regression specification:
    
    S(t) = a*X(t) + e 
    
    where S(t) represents current salaries, X(t) is a vector capturing performance related variables. 
    
    2. Ridge regression
    
    Ridge regression imposes a penalty on the size of the coefficients to reduce the variance of the estimates. Ridge regression works best in situations where the OLS estimates have high variances, which apply to our dataset.
    
    3. Lasso regression
    
    Different from Rdige regression, Lasso regression performs variable selections. The revised penalty allows coefficients to shrink towards exactly zero. Hence LASSO usually results into sparse models, that are easier to interpret.
    
    4. Regression with signals
    
    Yining insent here
    
    We get our best results from the Lasso regression, for which we are able to predict NBA player salaries with R^2 of 0.584.
    
   
    Along with the above models, we also computed statiscal scores in the following manner:
    
    Yining insert here. 
    
    
######Installation Instructions:

    1. Cloning the repository;
    2. Running the code on virtual machine requires installing the folowing packages: Numpy, Pandas, Sklearn, Request,bs4,etc (Please find the detailed list of packages in requirement.txt file).
    

######Description:
    
    STEP1: Download Libraries
    
    STEP2: Installing Packages
    
    Libraries and packages are specified in the Installation Instructions section above and in the corresponding sections of the master file: get_player_stat.ipynb.
    
    STEP3: Scraping the data
    
    To scrap the data from basketball-reference.com run scripts in the Section 3 Data Collection of the master file: get_player_stat.ipynb. The corresponding final pkl file is: tfa_working_ver_1. 
    
    The dataset consists of per game statistics including (Games, Games Started, Minutes Played Per Game, Field Goals Per Game, ..., Points Per Game) for 449 players in season 2017 - 2018 from the follwoing url:
    
    https://www.basketball-reference.com/leagues/NBA_2018_per_game.html    
    
    STEP4: Data cleaning

    In addition to these variables, we added team winning percentage during the regular season as an extra 
    
    There are five positions, for which we treated as a dummy variable
    
    We excluded any players with empty values and treated players who switched teams during the season as one single player. 
    
    
    STEP5: Analysis and Modeling
    
    We calculated correlations between different factors. We implemented the four models introduced in the Methodology and Models section, 
    
   
######Run Instructions:
     
     For all statistical analysis and regression results, run the code in the master file: get_player_stat.ipynb, and following the steps as specified in the description section above.






