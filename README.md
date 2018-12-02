Project Name: Predicting NBA Player Salary Upon Contract Expiration

Group Name: CoolPython

Group Members: Ayushmaan Kumar, Ankit Yadav, Yining Li, Chenjian Yang

Section 2


Background:

    The National Basketball Association (NBA) is a men’s professional basketball league in North America. Player salaries are affected by tons of factors, such as their age, position, experience, performance as reflected by various basic and advanced game statistics, their business value in terms of their fan base across the world and income outside the court. 
    
    We are curious about how much each of these factors contribute to their current salaries. For example, does age explain salaries to a certain extent? This project uses Python to analyze the relationship between salaris and the factors mentioned above and potentially develop models to predict individual player’s salaries based on these factors. Specifically the model takes individual players’ current year characteristics as inputs and returns their hypothetical predicted salaries. We are hopeful that our model would be of referential value to the general managers and individual players and their agents in negotiating the contracts. 


Methodology:
 
    1. Linear regression: 
    
    Multiple variable linear regression is the most natural first choice. Below is the regression specification:
    
    S(t) = a*X(t) + e 
    
    where S(t) represents current salaries, X(t) is a vector capturing performance related variables. The sample we are going to use is most likely going to be players who signed new contracts, excluding rookie players and those who take voluntary pay cuts.
   
    2. Lasso regression
    
    Update here
    
    3. Ridge regression
    
    Update here
    
    4. Regression with signals
    
    Update here
    
    Along with the above models models we have also prepared a statiscal score by using player statistics and then we are using that model to predict nba player salaries. With the help of our models, we are able to predict salaries of NBA players to an accuracy of about 55-60%.
    
    
Description:
    
    STEP1: Sraping the data
    
    To scrap the data from basketball-reference.com run the following scripts (can also be found in the master file: get_player_stat.ipynb)
    
    Description of the data here.
    
    
    STEP2: Conduct initial analysis
    
    We calculated correlations between different 
    
    
    STEP3: Run final regressions and construct predition model
    
    
Installation instructions (if any besides cloning the repo):

    Besides cloning the repository, if you are running the code on virtual machine you should install the folowing packages: Numpy, Pandas, Sklearn, Request,bs4,etc (Please find the detailed list of packages in requirement.txt file).

Run Instructions:
      
     - For statistical analysis and regression results, simply run the code in master file with file name: get_player_stat.ipynb
     - For predicting individual players' salaries, 





