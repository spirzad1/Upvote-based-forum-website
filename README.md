# Upvote-based-forum-website
A website/forum where game developers can directly communicate with their player base using reddit's upvote system to show the most important issues/topics that need to be addressed. Offers an solution to the growing disconnect between gaming companies and their player bases. 

Going to explore using a Reddit-clone code. This is because it shares many features I would like to implement into my own website such as comments, upvoting, and general post creation. I am going to be using flask as a web framework for my python code. 

# Step 1. Create a Virtual Environment and Install Dependencies
Create a new Virtual Environment for the project and source it. 

$ virtualenv venv

$ source venv/bin/activate

# Step 2. Setup the Database 
 Enter the MySQL shell and create a Flask app user and database running locally. 

mysql> create database reddit;

mysql> create user 'reddit'@'localhost' identified by 'reddit';

mysql> grant all privileges on reddit.* to 'reddit'@'localhost';
# Now apply the models defined in the flask app as such:

(venv) $ ./migrate.py db init

(venv) $ ./migrate.py db migrate

(venv) $ ./migrate.py db upgrade

Step 3. Run the server. 
