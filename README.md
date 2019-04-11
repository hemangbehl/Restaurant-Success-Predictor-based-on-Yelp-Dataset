# Restaurant-Success-Predictor-based-on-Yelp-Dataset
An end-sem group project done for the subject CMPE 255:Data Mining with a team of 3 people during Fall 2018 semester.

Objective: To develop models to help answer questions such as what attributes help in making a restaurant successful and what kind of restaurants are rated higher than others.

Performed pre-processing on over 6 GB of yelp JSON files and converted them into CSV format for better consumption and readability.
Performed data wrangling to obtain user patterns such as peak customer footfall and relation between noise levels and ratings.
Predicted the closure of a business with a F1 score of 73.10%.

Identified the locations and cuisine for a new restaurant to open with the best chance of success. [Done by another team member]

Predicted the ratings with a F1 score of 66.96% trained on over 2GB of Yelp review comments.

Classifiers Used : Naive Bayes, Random Forest, Linear SVC, Logistic Regression, XGBoost, KNeighbours, Decision Tree
Language and IDE : Python and Jupyter Notebook


----------------------
What each files does?

json_to_csv_converter_2.py		: convertes JSON into CSV file

Yelp_1.ipynb					: Converts the JSON files to CSV files using jupyter notebook. needs to specify file name.

Noise_level_effect_1.2.ipynb	: analysis on the noise level and star rating
									uses yelp_academic_dataset_business.csv, yelp_academic_dataset_review.csv

Footfall_1.3.ipynb				: analysis on the footfall pattern. Creates a new csv file: checkin_modified_all.csv
									uses yelp_academic_dataset_checkin.csv

Business_closure_1.8_final.ipynb: uses checkin_modified_all.csv and other files
									uses yelp_academic_dataset_business.csv, yelp_academic_dataset_review.csv and checkin_modified_all.csv

Yelp-read_3.ipynb				: requires datafiles yob in 'data/' folder
									creates a file names.csv
									exports unique name and its associated gender into name_gender.txt

Gender-names-use.ipynb			: uses name_gender.txt
									requires name_gender.txt to be in data/  folder
									converts it into a dictionary {name:gender}
									reads yelp_academic_dataset_user.csv
									uses the dictionary to map the names to the user's first name in the Yelp dataset
									inserts a new column Gender in it 
									exports this dataframe as modified_user_2.csv
									
Gender_diversity_1.3.ipynb		: uses modified_user_2.csv which contains user data + gender
									Percentage of genders: Female: 48%, Male:35%, Unknown:16%
									shows review count gender wise
									shows new users added per year gender wise
									
