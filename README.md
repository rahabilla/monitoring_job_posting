# Job Monitoring and Skill-Based Clustering System

This project automatically scrapes job postings from karkidi.com, clusters them according to the required skills using unsupervised machine learning, and notifies users when new job opportunities match their skill interests.

##  Features

- Scrapes the latest job postings including job title, company, location, and required skills  
- Clusters jobs by applying K-Means on TF-IDF vectors derived from required skills  
- Saves the trained model for reuse in classifying new postings  
- Allows users to select skill-based clusters to receive personalized job alerts  
- Supports automated daily scraping through schedulers like cron or APScheduler  
- Provides a Streamlit dashboard for interactive exploration of job listings  

## Data Collected

Each job record contains the following details:

- Job Title  
- Company Name  
- Required Skills  
- Location (when available)  

## Clustering Workflow

- **Preprocessing:** Clean the skills text, tokenize, and vectorize using TF-IDF  
- **Clustering:** Group jobs based on their skill vectors using K-Means  
- **Evaluation:** Performance assessed via silhouette score and manual review  
- **Matching:** User skill preferences are mapped to clusters to trigger alerts  

## Running the Dashboard

If the file `karkidi_jobs.csv` is not available locally, use the file uploader feature to upload the dataset and launch the dashboard via Streamlit.

##  Automation (Optional)

Utilize tools such as cron, APScheduler, or schedule to automate:

- Daily scraping (via `scraper.py`)  
- Classification and sending alerts  

## Requirements

For all necessary dependencies, refer to the `requirements.txt` file, which includes but is not limited to:

- streamlit  
- pandas  
- scikit-learn  
- nltk  
- beautifulsoup4  
- joblib  

## Future Improvements

- Integration of email alerts  
- Implementation of smart keyword extraction for enhanced clustering  
- NLP-based normalization of job titles  
