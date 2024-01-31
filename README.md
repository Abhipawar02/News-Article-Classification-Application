# News-Article-Classification-Application
A deployed streamlit Application to classify news articles, into following four categories:
    1. Business
    2. Entertainment 
    3. Sports
    4. World

application linnk - http://ec2-54-90-142-109.compute-1.amazonaws.com

## Getting Started

### Prerequisites

- Python 3.8.18
- Install required libraries: `pip install -r requirements.txt`

### Running the Script

1. Clone the repository: `git clone https://github.com/Abhipawar02/News-Article-Classification-Application.git` 
2. Navigate to the project directory: `cd News-Article-Classification-Application`
3. Run the script: `streamlit run app.py`

## Data Collection and Data Wrangling
- The raw data was collected from [Public News Website](https://indianexpress.com/).
- For detailed steps and code, refer to the [News Website-Scrapper](https://colab.research.google.com/drive/1gdkgr0gaqWT4HwUxo6iMaCf7_3D6ofoD?usp=sharing).  

### Check https://github.com/Abhipawar02/news-data-scrapping-and-section-classification Repository.

## Dataset

The raw dataset is included in the `dataset` directory, consisting of 193 entries with the following format:

- Article Title
- Article Body
- Section Value (Categorized into 'Entertainment', 'Business', 'World', 'Sport')

## Data Preprocessing
In order to prepare the dataset for analysis and modeling, the following data preprocessing steps were undertaken:
1. **Handling Null and Duplicated Values:**
   - Removed null values and duplicates, resulting in 128 non-null and unique entries.

2. **Visualizing Data Balance:**
   - Visualized the dataset to ensure a balanced distribution of entries within the 'Section_Value' categories ('Entertainment', 'Business', 'World', 'Sport').

3. **Creating 'Full Article' Column:**
   - Added a new column named 'Full Article' by combining the 'Article Title' and 'Article Body'.

4. **Text Cleaning with NLTK:**
   - Utilized the Natural Language Toolkit (NLTK) to perform the following text cleaning steps on the 'Full Article' column:
     - Removal of HTML tags.
     - Handling special characters.
     - Removal of stopwords.
     - Conversion of text to lowercase.
     - Lemmatization of words.

5. **Vectorization using Sklearn.CountVectorizer:**
   - Applied Sklearn's CountVectorizer to convert the 'Full Article' column into a numerical format suitable for machine learning models.

6. **Train-Test Split:**
   - Performed the train-test split to divide the dataset into training and testing sets for model training and evaluation.

## Hypertuning with sklearn Pipelines and MLFLOW integration
- To be add

## Model Evaluation, Selection And predict.py file
- To be add

## streamlit application 
- To be add

## DockerFile
- To be add

## AWS Setups  
- To be add

## Github Actions CI/CD Pipelines
- To be add

## Issues and Solutions
- To be add

## Security and Network Configure (AWS)
- To be add

## Ready to Share !
- To be add


