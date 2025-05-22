Skill-Based Job Monitoring & Clustering Tool
This project is designed to automatically fetch job listings from karkidi.com, group them based on required skillsets using unsupervised learning techniques, and notify users when new postings align with their interests.

 Key Highlights
Extracts job-related details such as title, company, skills, and location from karkidi.com

Applies K-Means clustering to TF-IDF-transformed skill descriptions

Saves the trained model for future use in classifying incoming job data

Lets users subscribe to clusters based on their preferred skills to receive updates

Supports automated scraping on a scheduled basis using tools like cron

Includes an interactive Streamlit dashboard to browse and filter job postings

 Information Collected
Each job entry includes the following:

Position title

Organization name

Skill requirements

Location (where available)

 Clustering Pipeline
Text Cleaning & Preprocessing: Skill text is cleaned, tokenized, and converted to TF-IDF vectors

Clustering: Jobs are grouped by similar skills using the K-Means algorithm

Assessment: Silhouette score and manual inspection are used to validate cluster quality

Job Matching: Clusters are linked to user-selected skill sets for notification purposes

 Setup Instructions
bash
Copy
Edit
git clone https://github.com/yourusername/job-clustering-dashboard.git
cd job-clustering-dashboard
pip install -r requirements.txt
 How to Launch the Dashboard
bash
Copy
Edit
streamlit run app.py
If the file karkidi_jobs.csv isn't present locally, the dashboard includes an uploader to manually load data.

 Optional Automation
Use task schedulers like cron, schedule, or APScheduler to automate:

The scraping process (scraper.py)

Classification and alert generation

 Tech Stack & Dependencies
Refer to requirements.txt for the complete list. Key packages used:

streamlit

scikit-learn

pandas

nltk

beautifulsoup4

joblib

 Potential Enhancements
Enable email-based notifications for matched jobs

Implement smarter skill extraction techniques

Normalize job titles using NLP-based approaches
