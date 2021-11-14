# Sector Coder Text Classifier

![image](https://storage.googleapis.com/sectorcoder/activity_code.png)

Humanitarian organizations use standardized **sector codes** to classify aid activities. This project will try to build a simple BERT classsifier able to assign sector codes to aid activities based on activity **titles** and paragraph length **descriptions**.

## Data

The project will use datasets stored in a public Google Cloud bucket for training and testing:
* One CSV file containing rows of activity **descriptions** *with* sector codes added by staff from humanitarian organizations + metadata listing corresponding reporting organization names, activity **titles** and sector code narratives (**activities.csv**): https://storage.googleapis.com/sectorcoder/activities.csv

* One CSV files containing rows of sector **codes** and their corresponding sentence length **descriptions** (file: **oecdcodes.csv**): https://storage.googleapis.com/sectorcoder/oecdcodes.csv

## Tasks

Under Construction

## Output

Given a list of aid activity titles and descriptions, the project will output corresponding codes assigned by the classifier. The classifier could also be setup to output more than one code based on likely matches.
