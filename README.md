Project Name: Predicting NBA Player Salary Upon Contract Expiration

Group Name: CoolPython

Group Members: Ayushmaan Kumar, Ankit Yadav, Yining Li, Chenjian Yang

Section 2


Background:

    The National Basketball Association (NBA) is a men’s professional basketball league in North America. Player salaries are affected by tons of factors, such as their age, position, experience, performance as reflected by various basic and advanced game statistics, their business value in terms of their fan base across the world and income outside the court. 
    
    We are curious about how much each of these factors contribute to their current salaries. For example, does the income out of basketball court explain wages to a certain extent? This project uses Python to develop a model predicting individual player’s wages based on the factors mentioned above. Specifically the model takes individual players’ current year characteristics as inputs and returns their predicted salaries in the following year. We are hopeful that our model would be of referential value to the general managers and individual players and their agents in negotiating the contracts. We will also explore the possibility of establishing a model to help teams find potential target players to acquire or trade in order to maximize their prospect of winning the championship.
    
    As far as methodology is concerned, we will mostly employ multiple linear regression. Below is the regression specification:
    
    S(t+1) = a*X(t) + b*Y(t) + c*Z(t) + e 
    
    where S(t+1) represents salaries in the following year, X(t), Y(t), and Z(t) are vectors capturing physical characteristics variables, performance related variables, and business value variables, respectively. The sample we are going to use is most likely going to be players who signed new contracts, excluding rookie players and those who take voluntary pay cuts.


Description:
    
    - A discription of what has been implemented
    - We first 

Installation instructions (if any besides cloning the repo):

    - Python packages should be listed appropriately in requirements.txt

Run Instructions:
     
     Testing: step 1

    - What do you need to type to get your program to do its thing
    - Take a hypothetical player A as an example. Player A has height...
    
How to Run the Code:

-If you are running the code on virtual machine you should install packages like: Numpy, Pandas, Sklearn, Request,bs4,etc ( Please find the detailed list of pakage in requirement.txt file)

-Run the code master file. (Filename: get_player_stat.ipynb)

-We are using the below statistical model for predicting the salary of the NBA players:

Linear regression
Lasso regression
Ridge regression

-Along with the above models models we have also prepared a statiscal score by using player statistics and then we are using that model to prodict nba player salary. 
With the help of our mdols we can able to predict salary of players to an accuracy of about 55-60%.



