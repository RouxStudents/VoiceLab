# Sector Coder Text Classifier

![image](https://storage.googleapis.com/sectorcoder/activity_code.png)

Humanitarian organizations use standardized **sector codes** to classify aid activities. This project will try to build a simple BERT classsifier able to assign sector codes to aid activities based on activity **titles** and paragraph length **descriptions**.

## Data

The project will use datasets stored in a public Google Cloud bucket for training and testing:
* One CSV file containing rows of activity **descriptions** *with* sector codes added by staff from humanitarian organizations + metadata listing corresponding reporting organization names, activity **titles** and sector code names (**activities.csv**): https://storage.googleapis.com/sectorcoder/activities.csv

* One CSV files containing rows of sector **codes**, sector **catagories** and their corresponding **names** and sentence length **descriptions** (file: **OECDSectorCodes.csv**): https://storage.googleapis.com/sectorcoder/OECDSectorCodes.csv

## Background

The humanitarian community has been working concertedly through the International Aid Transparency Initiative (**IATI**) to standardize how aid activitiers are reported and make the information accessible to machine applications. On a technical level, IATI is an XML standard and open data sharing channel. Aid activities can be reported in granular detail using 500 different standardized IATI elements and attributes. Additionally, non-standard elements and attributes can be added to XML files increase their granularity further. But generally, humanitarian organizations only use fraction of IATI's standardized elements and attributes.

A host of [vocabularlies](https://iatistandard.org/en/iati-standard/203/codelists/sectorvocabulary/) have been created for humanitarian organizations to use to classify aid activities. IATI encourages the use of **OECD DAC CRS Purpose Codes** organized into 3-digit catagories and 5-digit sector codes. Currrently, IATI contains information on over one million aid activities, many of these activities have been sector codes and many haven't. And of coded activities, most use OECD DAC purpose codes but many use other volcabularies.

Creating a classifier able to match activities and sector codes can make it possible to attach OECD DAC CRS sector codes to non-coded aid activities and to activities coded using differernt vocabularies.

## Tasks

* Initially, we would like to exlore building a classifier via a Google Colab notebook, to help document and arrange build steps, and TensorFlow.
* Prepare data
* Test setup and data loading
* ...


## Output

Given one or a list of aid activity titles and descriptions, the classifier will assign each activity a corresponding 3-digit sector category code and a 5-digit sector code. Where applicable, classifier will output more than one code based on likely matches.
