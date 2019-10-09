# Data Scientist Nanodegree (Term 2)

 Content for Udacity's Data Science Nanodegree curriculum, which includes project and lesson content.

 <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-nd/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License</a>. Please refer to [Udacity Terms of Service](https://www.udacity.com/legal) for further information.


# Project 1 - Data Science Blog Post

For this project, you will pick a dataset. Inspired by Robert, there are a few public datasets from AirBnB available below, but you may also choose a dataset similar to what was used in the lessons, or an entirely different dataset. Using your dataset, you will choose 3 questions you aspire to answer from the data.

### <a href="https://www.kaggle.com/stackoverflow/so-survey-2017">Stack Overflow Data - 2017 Survey</a>
You might have different questions about the 2017 StackOverflow survey data than I looked at earlier in the course. If you choose this dataset, you can not use the same questions that were analyzed earlier in the classroom.

Alternatively, if you felt pretty confident with the techniques in this lesson, you might be looking to push the envelope. In this case, you may choose to retrieve all of the <a href="https://insights.stackoverflow.com/survey">Stack Overflow Survey - Multiple Years</a> results. From this data, you could analyze trends over time. What languages were most popular in each year? What other changes can you observe over time?

### <a href="https://www.kaggle.com/airbnb/seattle/data">Seattle AirBNB Data</a>
The Seattle AirBnB homes data can be used at the above link. You might pair this with the Boston AirBnB data, which can be found at the link below.

### <a href="https://www.kaggle.com/airbnb/boston">Boston AirBNB Data</a>
If you are looking to really challenge yourself, data from Seattle and Boston AirBNB homes can be used to understand how much AirBNB homes are earning in certain time frames and areas. You can compare rates between the two cities, or try to understand if there is anything about the properties that helps you predict price. Can you find negative and positive reviews based on text? This dataset requires a number of skills beyond those shown thus far in the course, but if you would like a challenge, this will certainly test your ability to work with messy, real world data.

You can find additional AirBnB data at the link <a href="http://insideairbnb.com/get-the-data.html">here</a>.

## Choose A Dataset of Your Own
You are welcome to use Kaggle or another platform (or your own data) to create a blog and Github post instead of using the datasets discussed above.

## Key Steps for Project
Feel free to be creative with your solutions, but do follow the CRISP-DM process in finding your solutions.

#### 1) Pick a dataset.

#### 2) Pose at least three questions related to business or real-world applications of how the data could be used.

#### 3) Create a Jupyter Notebook, using any associated packages you'd like, to:

##### Prepare data:

- Gather necessary data to answer your questions
- Handle categorical and missing data
- Provide insight into the methods you chose and why you chose them

##### Analyze, Model, and Visualize

- Provide a clear connection between your business questions and how the data answers them.

#### 4) Communicate your business insights:

- Create a Github repository to share your code and data wrangling/modeling techniques, with a technical audience in mind
- Create a blog post to share your questions and insights with a non-technical audience

Your deliverables will be a Github repo and a blog post. Use the <a href="https://review.udacity.com/#!/rubrics/1507/view">rubric</a> to assist in successfully completing this project!


# Project 2 - Disaster Response Pipelines

## Project Overview
In this course, you've learned and built on your data engineering skills to expand your opportunities and potential as a data scientist. In this project, you'll apply these skills to analyze disaster data from <a href="https://www.figure-eight.com/">Figure Eight</a> to build a model for an API that classifies disaster messages.

In the Project Workspace, you'll find a data set containing real messages that were sent during disaster events. You will be creating a machine learning pipeline to categorize these events so that you can send the messages to an appropriate disaster relief agency.

Your project will include a web app where an emergency worker can input a new message and get classification results in several categories. The web app will also display visualizations of the data. This project will show off your software skills, including your ability to create basic data pipelines and write clean, organized code!

Below are a few screenshots of the web app.

![overview chart](https://video.udacity-data.com/topher/2018/September/5b967bef_disaster-response-project1/disaster-response-project1.png)

![result messages](https://video.udacity-data.com/topher/2018/September/5b967cda_disaster-response-project2/disaster-response-project2.png)


## Project Components
There are three components you'll need to complete for this project.

### 1. ETL Pipeline
In a Python script, process_data.py, write a data cleaning pipeline that:

Loads the messages and categories datasets
Merges the two datasets
Cleans the data
Stores it in a SQLite database

### 2. ML Pipeline
In a Python script, train_classifier.py, write a machine learning pipeline that:

Loads data from the SQLite database
Splits the dataset into training and test sets
Builds a text processing and machine learning pipeline
Trains and tunes a model using GridSearchCV
Outputs results on the test set
Exports the final model as a pickle file

### 3. Flask Web App
We are providing much of the flask web app for you, but feel free to add extra features depending on your knowledge of flask, html, css and javascript. For this part, you'll need to:

Modify file paths for database and model as needed
Add data visualizations using Plotly in the web app. One example is provided for you
Github and Code Quality
Your project will also be graded based on the following:

Use of Git and Github
Strong documentation
Clean and modular code
Follow the RUBRIC when you work on your project to assure you meet all of the necessary criteria for developing the pipelines and web app.


## Project Details
Below are additional details about each component and tips to get you started.

### Data Pipelines: Jupyter Notebooks
We've provided Jupyter notebooks in Project Workspaces with instructions to get you started with both data pipelines. The Jupyter notebook is not required for submission, but highly recommended to complete before getting started on the Python script.

### Project Workspace - ETL
The first part of your data pipeline is the Extract, Transform, and Load process. Here, you will read the dataset, clean the data, and then store it in a SQLite database. We expect you to do the data cleaning with pandas. To load the data into an SQLite database, you can use the pandas dataframe .to_sql() method, which you can use with an SQLAlchemy engine.

Feel free to do some exploratory data analysis in order to figure out how you want to clean the data set. Though you do not need to submit this exploratory data analysis as part of your project, you'll need to include your cleaning code in the final ETL script, process_data.py.

### Project Workspace - Machine Learning Pipeline
For the machine learning portion, you will split the data into a training set and a test set. Then, you will create a machine learning pipeline that uses NLTK, as well as scikit-learn's Pipeline and GridSearchCV to output a final model that uses the message column to predict classifications for 36 categories (multi-output classification). Finally, you will export your model to a pickle file. After completing the notebook, you'll need to include your final machine learning code in train_classifier.py.

### Data Pipelines: Python Scripts
After you complete the notebooks for the ETL and machine learning pipeline, you'll need to transfer your work into Python scripts, process_data.py and train_classifier.py. If someone in the future comes with a revised or new dataset of messages, they should be able to easily create a new model just by running your code. These Python scripts should be able to run with additional arguments specifying the files used for the data and model.

Example:
python process_data.py disaster_messages.csv disaster_categories.csv DisasterResponse.db

python train_classifier.py ../data/DisasterResponse.db classifier.pkl
Templates for these scripts are provided in the Resources section, as well as the Project Workspace IDE. The code for handling these arguments on the command line is given to you in the templates.

### Flask App
In the last step, you'll display your results in a Flask web app. We have provided a workspace for you with starter files. You will need to upload your database file and pkl file with your model.

This is the part of the project that allows for the most creativity. So if you are comfortable with html, css, and javascript, feel free to make the web app as elaborate as you would like.

In the starter files, you will see that the web app already works and displays a visualization. You'll just have to modify the file paths to your database and pickled model file as needed.

There is one other change that you are required to make. We've provided code for a simple data visualization. Your job will be to create two additional data visualizations in your web app based on data you extract from the SQLite database. You can modify and copy the code we provided in the starter files to make the visualizations.

### Github and Code Quality
Throughout the process, make sure to push your code and comments to Github so that you will not repeat your work and you can keep track of the changes you've made. This will also help you keep your code modular and well documented. Make sure to include effective comments and docstrings. These software engineering practices will improve your communication and collaboration in the future when you work within a team.

### <a href="https://s3.amazonaws.com/video.udacity-data.com/topher/2018/March/5a9834fd_data-pipeline/data-pipeline.py">Starter Code</a>
The coding for this project can be completed using the Project Workspace IDE provided. Here's the file structure of the project:

- app
| - template
| |- master.html  # main page of web app
| |- go.html  # classification result page of web app
|- run.py  # Flask file that runs app

- data
|- disaster_categories.csv  # data to process 
|- disaster_messages.csv  # data to process
|- process_data.py
|- InsertDatabaseName.db   # database to save clean data to

- models
|- train_classifier.py
|- classifier.pkl  # saved model 

- README.md
Running the Web App from the Project Workspace IDE
When working in the Project Workspace IDE, here is how to see your Flask app.

Open a new terminal window. You should already be in the workspace folder, but if not, then use terminal commands to navigate inside the folder with the run.py file.

Type in the command line:

python run.py
Your web app should now be running if there were no errors.

Now, open another Terminal Window.

Type

env|grep WORK
You'll see output that looks something like this:


In a new web browser window, type in the following:

https://SPACEID-3001.SPACEDOMAIN
In this example, that would be: "https://viewa7a4999b-3001.udacity-student-workspaces.com/" (Don't follow this link now, this is just an example.)

Your SPACEID might be different.

You should be able to see the web app. The number 3001 represents the port where your web app will show up. Make sure that the 3001 is part of the web address you type in.

<a href="https://review.udacity.com/#!/rubrics/1565/view">Rubric</a>
Follow the Rubric when you work on your project to assure you meet all of the necessary criteria for developing the pipelines and web app.


# Project 3 - Recommendations with IBM


## Introduction
For this project you will analyze the interactions that users have with articles on the IBM Watson Studio platform, and make recommendations to them about new articles you think they will like. Below you can see an example of what the dashboard could look like displaying articles on the IBM Watson Platform.

Though the above dashboard is just showing the newest articles, you could imagine having a recommendation board available here that shows the articles that are most pertinent to a specific user.

In order to determine which articles to show to each user, you will be performing a study of the data available on the IBM Watson Studio platform. You can create your own account to become a part of their community, and get a better understanding of their data by creating an account on the platform here.


## Your Tasks
Your project will be divided into the following tasks

### I. Exploratory Data Analysis

Before making recommendations of any kind, you will need to explore the data you are working with for the project. Dive in to see what you can find. There are some basic, required questions to be answered about the data you are working with throughout the rest of the notebook. Use this space to explore, before you dive into the details of your recommendation system in the later sections.

### II. Rank Based Recommendations

To get started in building recommendations, you will first find the most popular articles simply based on the most interactions. Since there are no ratings for any of the articles, it is easy to assume the articles with the most interactions are the most popular. These are then the articles we might recommend to new users (or anyone depending on what we know about them).

### III. User-User Based Collaborative Filtering

In order to build better recommendations for the users of IBM's platform, we could look at users that are similar in terms of the items they have interacted with. These items could then be recommended to the similar users. This would be a step in the right direction towards more personal recommendations for the users. You will implement this next.

### IV. Content Based Recommendations (EXTRA - NOT REQUIRED)

Given the amount of content available for each article, there are a number of different ways in which someone might choose to implement a content based recommendations system. Using your NLP skills, you might come up with some extremely creative ways to develop a content based recommendation system. You are encouraged to complete a content based recommendation system, but not required to do so to complete this project.

### V. Matrix Factorization

Finally, you will complete a machine learning approach to building recommendations. Using the user-item interactions, you will build out a matrix decomposition. Using your decomposition, you will get an idea of how well you can predict new articles an individual might interact with (spoiler alert - it isn't great). You will finally discuss which methods you might use moving forward, and how you might test how well your recommendations are working for engaging users.


## Gather Submission Materials
Either submit your project from the workspace OR here - not both.

Once you are satisfied with the status of your Notebook, you should save it in a format that will make it easy for others to read. You can use the File -> Download as -> HTML (.html) menu to save your notebook as an .html file. If you get an error about "No module name", then open a terminal and try installing the missing module using pip install <module_name> (don't include the "<" or ">" or any words following a period in the module name).

You will submit both your original Notebook and an HTML or PDF copy of the Notebook for review. There is no need for you to include any data files with your submission. If you made reference to other websites, books, and other resources to help you in solving tasks in the project, make sure that you document them. It is recommended that you either add a "Resources" section in a Markdown cell at the end of the Notebook report, or you can include a readme.txt file documenting your sources.


## Submit the Project
When you're ready, double check the project <a href="https://review.udacity.com/#!/rubrics/2322/view">RUBRIC</a>, make revisions as needed, then click on the "Submit Project" button to go to the project submission page. You can submit your files as a .zip archive or you can link to a GitHub repository containing your project files. If you go with GitHub, note that your submission will be a snapshot of the linked repository at time of submission. It is recommended that you keep each project in a separate repository to avoid any potential confusion: if a reviewer gets multiple folders representing multiple projects, there might be confusion regarding what project is to be evaluated.

It can take us up to a week to grade the project, but in most cases it is much faster. You will get an email once your submission has been reviewed. In the meantime, you should feel free to continue on with your learning journey by continuing on to the next module in the program.



# Project 4 [Option 1] - Dog Breed Classification

### Project Overview
Welcome to the dog breed classifier project. This project uses Convolutional Neural Networks (CNNs)! In this project, you will learn how to build a pipeline to process real-world, user-supplied images. Given an image of a dog, your algorithm will identify an estimate of the canine’s breed. If supplied an image of a human, the code will identify the resembling dog breed.

If you choose to complete this project, there are additional lessons in the extracurricular section of the classroom that you will likely find useful.

### Reminder
If you choose to complete the dog breed classifier project, you still must meet expectations for all the <a href="https://review.udacity.com/#!/rubrics/2345/view">RUBRIC</a> items associated with the Data Scientist Capstone project. That is, you still must deploy your code into an application, or you must write a post to be shared about the technical details of your analysis. The workspace on the next page walks you through one possible solution, but you are welcome to discuss other solutions that are much different.



# Project 4 [Option 2] - Starbucks Customer Behavior
<a href="https://www.youtube.com/watch?v=bq-H7M5BU3U">Overview Video</a>

# Project 4 [Option 3] - Arvato Customer Segmentation

<a href="https://www.youtube.com/watch?v=qBR6A0IQXEE">Overview Video</a>
## Create a Customer Segmentation Report for Arvato Financial Solutions
To introduce yourself to the scenario you'll be investigating in this capstone project option, take a look at the following video with Timo Reis from Arvato Financial Solutions.

## Hiring Opportunity
The data and outline of this project was provided by Arvato Financial Solutions, a Bertelsmann subsidiary. High performers on this project will have their Udacity profile sent directly to Arvato for review, and may lead to an interview at either Arvato or Bertelsmann. This is a tremendous opportunity to get access to a data science hiring manager!

## Steps to Complete This Project
The project has three major steps: the customer segmentation report, the supervised learning model, and the Kaggle Competition.

### 1. Customer Segmentation Report
This section will be similar to the corresponding project in Term 1 of the program, but the datasets now include more features that you can potentially use. You'll begin the project by using unsupervised learning methods to analyze attributes of established customers and the general population in order to create customer segments.

### 2. Supervised Learning Model
You'll have access to a third dataset with attributes from targets of a mail order campaign. You'll use the previous analysis to build a machine learning model that predicts whether or not each individual will respond to the campaign.

### 3. Kaggle Competition
Once you've chosen a model, you'll use it to make predictions on the campaign data as part of a Kaggle Competition. You'll rank the individuals by how likely they are to convert to being a customer, and see how your modeling skills measure up against your fellow students.



# Project 4 [Option 4] - Spark for Customer Churn Prediction

<a href="https://www.youtube.com/watch?v=lPCzCEG2yRs">Overview Video</a>
### What will I learn?
You'll learn how to manipulate large and realistic datasets with Spark to engineer relevant features for predicting churn. You'll learn how to use Spark MLlib to build machine learning models with large datasets, far beyond what could be done with non-distributed technologies like scikit-learn.

### Career Relevance
Predicting churn rates is a challenging and common problem that data scientists and analysts regularly encounter in any customer-facing business. Additionally, the ability to efficiently manipulate large datasets with Spark is one of the highest-demand skills in the field of data.

### Essential Skills
Load large datasets into Spark and manipulate them using Spark SQL and Spark Dataframes
Use the machine learning APIs within Spark ML to build and tune models
Integrate the skills you've learned in the Spark course and the Data Scientist Nanodegree program
Take the Spark Course

You can find the Spark course in your Extracurriculars section.

### Project Instructions
The full dataset is 12GB, of which you can analyze a mini subset in the workspace on the following page. Optionally, you can choose to follow the instructions in the Extracurricular course to deploy a Spark cluster on the cloud using AWS or IBM Cloud to analyze a larger amount of data. Currently we have the full 12GB dataset available to you if you use AWS. If you use IBM, you can download a medium sized dataset to upload to your cluster.

Details on how to do this using AWS or IBM Cloud are included in the last lesson of the Extracurricular Spark Course content linked above. Note that this part is optional, and you will not receive credits to fund your deployment. You can do the IBM portion for free. Using AWS will cost you around $30 if you run a cluster up for a week with the settings we provide.

Once you've built your model, either in the classroom workspace or in the cloud with AWS or IBM, download your notebook and complete the remaining components of your Data Scientist Capstone project, including thorough documentation in a README file in your Github repository, as well as a web app or blog post explaining the technical details of your project. Be sure to review the Project <a href="https://review.udacity.com/#!/rubrics/2345/view">RUBRIC</a> thoroughly before submitting your project.

### Submission Instructions
Create a GitHub repository for this project, containing your notebook and README file. Once your project is finished, submit the URL of this repository.
