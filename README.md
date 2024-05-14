# Big-Data-Tools-Techniques-Project
For your second task, you are working with a dataset extracted from Steam, an online video 
game distribution service. This dataset is available on Blackboard and named steam200k.csv. It provides details on the games different members have purchased and played, 
along with the number of hours they have played each game. It contains four columns:
➢The first column contains a unique identifier for each member
➢The second column contains the name of the game they purchased or played
➢The third column contains details of the member behaviour, either ‘purchase’ or 
‘play’. Because a game has to be purchased before it can be played there will be two 
entries for the same game / member combination in some instances
➢The fourth is set to 1 for rows where the behaviour is ‘purchase’. For rows where the 
behavious is ‘play’ the value in the fourth column corresponds to the number of 
hours of play
We can use both purchase and play behaviours as implicit user feedback, which is useful for 
training a recommender system.
Your task as a data scientist is to do the following:
➢ Load the dataset into a Spark DataFrame. You may want to consider carrying out 
some initial exploratory analysis of the data, which you are welcome to do using 
DataFrames, Spark SQL, Databricks visualisations, another visualisation library etc.
➢ Use MLlib to train a collaborative filtering recommender system on the provided 
data, evaluate its performance and explore some of the resulting 
recommendations. You will need to carry out all pre-processing steps, such as 
splitting the data into training and test sets. It is your decision whether to include 
both ‘purchase’ and ‘play’ behaviours or to choose one of these as more suitable
for your purposes. You may wish to experiment with more than one approach.
Note: To run Alternating Least Squares (ALS) matrix factorization using MLlib, we need to 
have integer ID values for both users and items, and this dataset does not contain IDs for 
the games. You will need to find a way to generate a unique integer ID for each game and 
add this into the DataFrame. There is an additional file, games.csv, which you can use to 
do this, but you will receive more marks if you are able to complete this within Databricks 
without using this additional csv file.
2.2.2. Extra features to be implemented for extra marks.
For this task, an implementation of the above which is correct, fully documented and 
clearly explained can only receive a maximum mark of 69% for this component. Higher 
scoring submissions will need to implement additional features, such as:
Assessment Information/Brief
9
➢ You can receive more marks for multiple runs as part of your experiment, for 
example, training models with different hyperparameters.
➢ Track your experiment with MLflow. You must include screenshots from the 
Databricks Experiment UI in your report to evidence that you have done this.
➢ More in-depth data exploration / visualisation of the data, and more in-depth 
exploration and evaluation of the recommendations generated. For example, you 
may want to summarise and visualise information such as the most frequently 
purchased games and the games with the highest total ‘play’ time
