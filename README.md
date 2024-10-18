# **Project Title**
Speed-Related Highway Accident: Vehicle Collisions in the UK Analysis - 2004 - 2014

**Project Description**
This project aims at analyzing car-to-car collisions in the UK between the years 2004 and 2014, focusing on particular accidents identified as speed-related. The intent of the analysis is guided by answering some key questions that will help in identifying what really causes highway accidents, especially those related to overspeeding. 

Objectives
The major objectives of this analysis include:

Answering Key Questions:

Identify meaningful patterns in vehicle collisions, especially regarding speeding.

Assess how factors like location, weather, and road conditions affect accidents.

Demonstrating Data Analysis Competencies:

Show the ability to understand how data are structured and the types of data common in vehicle accident analysis.

Do data wrangling, which is the process of cleaning and transforming data to prepare for analysis.

Dataframe Manipulation & Joins:

Apply methods such as joining multiple datasets and manipulating dataframes to gain further insight.

Handling of Missing Data:

Show how missing data-a common feature of most real-world datasets-can be treated and discuss the implications of missing values on the analysis.

**Dataset**
The dataset used for the project was found on Kaggle and focused on vehicle collisions in the UK from 2004 to 2014. The following are included in the dataset:

Accident Information: Time and date of accidents, location, and severity of accidents.
Conditions: Road and weather conditions at the moment of each accident.
Speeding: Whether speeding was involved as a cause in the accident.
Other factors: Human error, road infrastructure, and traffic flows at a given time.

**Key Features**
This project will look for answers to the following questions:
a) What % of all accidents is due to speed, and what is its severity?
b) How does weather and road conditions influence when speed-related accidents occur?
Which times of day, or which locations, in the UK have the most speed-related accidents?
Tools & Libraries Used
For this analysis, the following Python libraries are employed:

Pandas: Loading, cleaning, manipulating data
NumPy: For numerical calculations
Matplotlib & Seaborn: Presenting trends and relationships across data, such as frequency of accident by region or time of day
Scikit-learn: To build machine learning models, if predictive modeling is to be done.

# **Process and Analysis**
Loading the Dataset

First, there is loading of the dataset, which was through the use of pandas.read_csv() to import accident data into a pandas DataFrame. The dataset to be used in this case is UK vehicle accident information, which went into the following variable:

data = pd.read_csv('/content/drive/MyDrive/Accidents0514.csv')

Splitting Data

After the data were loaded, some of the steps included splitting up the data into a training and testing set. This is through the use of a method from sklearn commonly known as train_test_split(). For this, 80% of the data will be used for training, while the remaining 20% will be used for testing.

train_frame, test_frame = train_test_split(data, test_size=0.2, random_state=42)

The test_size=0.2 indicates that 20% of the data is reserved for the test set, while 80% will be used to train the model.

Checking Dataset Size

After the splitting of data into training and test datasets, I checked the shape -size- of each to make sure the split was correctly done. The .shape method returns the dimension of the DataFrame:
The Training set, comprising 1,312,477 rows and 32 columns:

train_frame.shape
Test set: 328,120, 32

test_frame.shape

Data Structure Understanding

This dataset consists of 32 feature columns in total, describing the location of the accident, the time of the accident, the weather condition, severity of the accident, and whether speeding was involved. These features will be used later in analyses to build machine learning models that predict things such as accident severity based on speed and other variables.

# **Model Construction**
In this analysis, several models are built to predict the accident likelihood based on different contributing factors, as described below:

Vanilla Model: The simplest neural network to establish a performance baseline.

L1 Regularization Models: To introduce sparsity and improve feature selection.

L2 Regularization Models: To penalize large weights, reduce overfitting.
Optimizers Used: Adam and RMSProp; early stopping strategies were adopted to help improve training efficiency and model generalization.

**Results and Discussion**
The results from the analysis provide vital features of speed-related highway crashes. These will give very valuable insights into the variables which drive the severity of collisions. A number of visualizations, including bar charts, heatmaps, and scatter plots, are used to show the relationships and trends within the data.

**Conclusion**
The project in itself epitomizes competence in the analysis of real-world data, extracting insights from the said data, and coming up with predictive models that explain vehicle collisions, whose findings should in turn ideally make improvements in road safety, or at best improve awareness in speed-related incidents.