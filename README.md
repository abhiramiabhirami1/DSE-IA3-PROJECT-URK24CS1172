# MentorMatch: Data Science-Based Mentor Recommendation System

## Project Overview

MentorMatch is a Data Science project that aims to connect students and professionals with suitable industry mentors based on their career goals, skills, experience level, industry interests, and mentor availability.

Finding the right mentor can be challenging, especially for students who are beginning their careers. MentorMatch uses data analysis and a content-based recommendation approach to help users identify mentors whose skills and professional backgrounds align with their learning needs.

This project demonstrates how Data Science and Machine Learning techniques can support personalized mentor recommendations.

## Problem Statement

Students and early-career professionals often struggle to find suitable mentors who can guide them toward their career goals. Manual mentor selection can be time-consuming and may not adequately consider individual skills, interests, or experience levels.

The objective of this project is to develop a data-driven system that analyzes mentor profiles and recommends relevant mentors to candidates.

## Objectives

- Analyze and understand mentor profile data.
- Clean and preprocess the dataset.
- Perform Exploratory Data Analysis (EDA) and descriptive statistics.
- Apply statistical inference to explore patterns in mentor data.
- Build a content-based mentor recommendation system.
- Explore mentor profile groups using unsupervised learning.
- Evaluate recommendation performance using suitable metrics.
- Provide an interactive interface for candidate submissions.
- Support batch recommendations through an optional candidate CSV upload.

## Technologies Used

- **Programming Language:** Python
- **Platform:** Google Colab
- **Data Processing:** Pandas, NumPy
- **Data Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn
- **Text Processing:** TF-IDF Vectorization and Cosine Similarity
- **Statistical Analysis:** SciPy
- **Interactive Interface:** IPython Widgets
- **Dataset Format:** CSV

## Dataset Description

The project uses `mentor_dataset.csv`, which contains sample mentor profiles.

The dataset includes the following fields:

| Column | Description |
|---|---|
| `mentor_id` | Unique identifier for each mentor |
| `name` | Mentor name used in the sample dataset |
| `skills` | Skills and technical or professional expertise |
| `career_goal` | Career path associated with the mentor |
| `level` | Experience or guidance level |
| `industry` | Mentor's industry category |
| `years_experience` | Years of professional experience |
| `rating` | Sample mentor rating |
| `completed_sessions` | Sample number of completed mentoring sessions |
| `availability` | General availability for mentoring |

**Dataset note:** The current dataset contains synthetic sample records created for academic demonstration. Names, ratings, and session counts should not be treated as verified real-world information.

An optional `candidate_requests.csv` file can be used to submit multiple candidate requests for batch recommendations. It requires at least the `career_goal` and `skills` columns.

## Project Workflow

1. **Data Loading:** Upload and load the mentor dataset into Google Colab.
2. **Data Cleaning:** Check missing values, duplicates, column types, and data quality.
3. **Exploratory Data Analysis:** Visualize mentor skills, industries, ratings, experience, and completed sessions.
4. **Descriptive Statistics:** Summarize numerical and categorical variables.
5. **Statistical Inference:** Conduct a statistical test to investigate differences between selected mentor groups.
6. **Recommendation System:** Represent mentor profiles using TF-IDF and compare candidate requirements with mentor profiles using cosine similarity.
7. **Model Evaluation:** Evaluate recommendations using ranking metrics such as Precision@K, Recall@K, and NDCG@K, where applicable.
8. **Unsupervised Learning:** Apply K-Means clustering to explore groups of mentors based on numerical profile features.
9. **Interactive Demo:** Accept candidate details and display suitable mentor recommendations.
10. **Batch Submission:** Optionally process a CSV containing several candidate requests and export recommendation results.

## Recommendation System

MentorMatch uses a content-based recommendation approach.

The system compares candidate information, including career goals and skills, with the available mentor profiles.

### How It Works

1. Mentor skills and career-related text are combined into profile descriptions.
2. TF-IDF converts text into numerical feature vectors.
3. Cosine similarity measures how closely candidate requirements match mentor profiles.
4. Mentors are ranked according to similarity scores.
5. The system displays the top-ranked mentors for the candidate.

The recommendations are based on profile similarity and do not guarantee mentoring quality or successful career outcomes.

## Model Evaluation

The project can use the following metrics to assess recommendation ranking:

- **Precision@K:** Measures the proportion of the top K recommendations considered relevant.
- **Recall@K:** Measures the proportion of relevant mentors retrieved in the top K recommendations.
- **NDCG@K:** Evaluates recommendation ranking by giving greater importance to relevant mentors appearing higher in the list.

If relevance labels are generated from the same profile attributes used by the recommender, the resulting metrics are only a demonstration of the evaluation process. They are not independent evidence of real-world recommendation quality. Reliable real-world evaluation would require independently collected candidate feedback or expert relevance judgments.

## Unsupervised Learning

K-Means clustering is used to explore possible groups among mentor profiles using numerical features such as:

- Years of experience
- Mentor rating
- Completed mentoring sessions

Features should be standardized before clustering because they use different numerical scales. The silhouette score can help compare clustering configurations.

The resulting clusters are exploratory groups, not definitive categories of mentor quality.

## How to Run the Project

### Requirements

- A Google account
- Internet access
- A web browser
- The project Jupyter notebook (`.ipynb`)
- The `mentor_dataset.csv` file

### Steps

1. Open [Google Colab](https://colab.research.google.com/).
2. Open the project notebook from GitHub or upload the `.ipynb` file.
3. Run the notebook cells in order.
4. When prompted, upload `mentor_dataset.csv`.
5. Review the data cleaning output, visualizations, statistical analysis, recommendation results, and clustering results.
6. Use the interactive candidate form to enter a career goal and skills.
7. Optionally upload `candidate_requests.csv` to generate recommendations for multiple candidates.
8. Download the generated recommendation results if the notebook provides the download option.

**Important:** Run the cells in sequence so that required variables and functions are defined before they are used.

## Expected Outcomes

- A cleaned and analyzed mentor dataset.
- Visualizations and descriptive statistics.
- Statistical analysis of selected mentor characteristics.
- A content-based mentor recommendation prototype.
- Recommendation evaluation results.
- Exploratory mentor clusters.
- An interactive candidate submission demo.
- Optional downloadable batch recommendation results.

Actual outputs depend on the dataset and the notebook implementation.

## Limitations

- The dataset contains synthetic sample records rather than verified mentor profiles.
- Ratings and completed session counts are illustrative.
- Profile similarity does not establish the actual quality of a mentor.
- Real-time calendar scheduling, video calls, and chat are not implemented unless separately integrated.
- The system requires real user feedback and independent relevance judgments for meaningful real-world evaluation.
- Recommendations may reflect gaps or biases in the available profile data.

## Ethical Considerations

- Protect candidate and mentor personal information.
- Obtain consent before collecting or using personal data.
- Avoid using sensitive personal attributes to determine recommendations.
- Evaluate whether recommendations unfairly exclude certain groups.
- Clearly communicate that recommendations are suggestions, not guarantees.
- Use verified profiles and transparent evaluation procedures before deploying the system in a real environment.

## Future Enhancements

- Integrate calendar availability and automated meeting scheduling.
- Add video conferencing and mentor-candidate messaging.
- Collect user feedback to improve recommendations.
- Evaluate the recommender using independently labeled relevance data.
- Develop a web application using Flask, Django, or FastAPI.
- Add secure user authentication and profile management.
- Integrate a database for storing mentor profiles and candidate requests.
- Deploy the application for real-world testing after privacy, security, and fairness reviews.

## Conclusion

MentorMatch demonstrates how Data Science techniques can be applied to a practical career-guidance problem. By combining data cleaning, exploratory analysis, statistical inference, content-based recommendation, and clustering, the project provides an academic prototype for matching candidates with potentially suitable mentors.

The project can be extended into a more complete mentoring platform through real-world data collection, independent evaluation, scheduling integration, and a user-friendly web application.

## Academic Context

**Project:** MentorMatch – Data Science-Based Mentor Recommendation System  
**Course Area:** Data Science  
**Platform:** Google Colab  
**Repository:** [DSE-IA3-PROJECT-URK24CS1172](https://github.com/abhiramiabhirami1/DSE-IA3-PROJECT-URK24CS1172)

## References

1. Pedregosa, F., et al. (2011). *Scikit-learn: Machine Learning in Python.* Journal of Machine Learning Research, 12, 2825–2830.
2. Scikit-learn documentation: https://scikit-learn.org/stable/
3. Pandas documentation: https://pandas.pydata.org/docs/
4. NumPy documentation: https://numpy.org/doc/
5. SciPy documentation: https://docs.scipy.org/doc/scipy/
6. Matplotlib documentation: https://matplotlib.org/stable/
7. Seaborn documentation: https://seaborn.pydata.org/
8. Google Colab: https://colab.research.google.com/
