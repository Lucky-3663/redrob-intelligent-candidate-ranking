# Intelligent Candidate Discovery & Ranking System

AI-powered candidate discovery and ranking system developed for the Redrob Data & AI Challenge. The solution combines candidate skills, experience, role relevance, and engagement signals to generate explainable rankings.

Overview

This project was developed for the Redrob Data & AI Challenge.

The objective is to build an intelligent candidate ranking system that helps recruiters identify the most relevant candidates from a large talent pool using candidate attributes such as experience, AI-related skills, professional role, and recruiter engagement signals.

The system generates a ranked list of candidates with explainable scoring and reasoning.

⸻

Problem Statement

Recruiters often face challenges while screening thousands of candidate profiles.

Traditional keyword-based matching systems fail to distinguish between:

* Candidates with genuine AI/ML experience.
* Candidates who simply list AI-related keywords.
* Candidates who are unlikely to respond to recruiter outreach.

The goal is to create a ranking framework that prioritizes candidate quality, relevance, and engagement likelihood.

⸻

Dataset Features

The dataset contains the following attributes:

Feature	Description
candidate_id	Unique candidate identifier
current_role	Candidate’s current job role
experience_years	Total years of experience
ai_core_skills	Number of AI-related skills
response_rate	Historical recruiter response rate

⸻

Approach

1. Data Processing

* Load candidate records.
* Validate and clean data.
* Normalize numerical features.
* Prepare ranking inputs.

2. Feature Engineering

The following candidate signals were used:

AI Skill Score

Measures the number of AI-related skills possessed by a candidate.

Experience Score

Evaluates professional experience and industry exposure.

Engagement Score

Uses recruiter response rate as a proxy for candidate availability and responsiveness.

Role Relevance Score

Measures alignment between the candidate’s current role and AI-focused opportunities.

⸻

Ranking Methodology

A weighted scoring framework was used:

Final Score =
40% × AI Skills +
25% × Experience +
20% × Response Rate +
15% × Role Relevance

Where:

* AI Skills reward technical competency.
* Experience rewards practical expertise.
* Response Rate rewards recruiter engagement probability.
* Role Relevance rewards domain alignment.

Candidates are ranked in descending order of the final score.

⸻

Pipeline

1. Load Dataset
2. Data Cleaning
3. Feature Extraction
4. Score Computation
5. Candidate Ranking
6. Result Generation
7. CSV Export

⸻

Output Format

The final output contains:

Column	Description
candidate_id	Candidate Identifier
rank	Candidate Rank
score	Final Match Score
reasoning	Explanation for ranking

Example:

candidate_id,rank,score,reasoning

CAND_0004989,1,0.9920,“HR Manager with 6.1 yrs; 9 AI core skills; response rate 0.76”

⸻

Technologies Used

* Python
* Pandas
* NumPy
* Scikit-Learn
* Jupyter Notebook

⸻

Repository Structure

project/
│
├── data/
│   └── candidates.csv
│
├── outputs/
│   └── ranked_candidates.csv
│
├── notebooks/
│   └── ranking_analysis.ipynb
│
├── src/
│   └── ranking_pipeline.py
│
├── requirements.txt
│
└── README.md

⸻

Results

The system successfully generates a ranked list of candidates based on skill coverage, experience, recruiter responsiveness, and role relevance.

The ranking process enables:

* Faster candidate screening
* Improved recruiter efficiency
* Scalable candidate evaluation
* Explainable ranking decisions

⸻

Future Improvements

* Semantic candidate-job matching using embeddings.
* Transformer-based candidate ranking.
* Learning-to-Rank (LTR) models.
* Recruiter feedback loops.
* Real-time recommendation systems.
* Hybrid retrieval and ranking architecture.

⸻

Challenge Submission

Deliverables:

* GitHub Repository
* Project Presentation (PDF)
* Ranked Output CSV/XLSX

⸻

Author

Participant: [Your Name]

Redrob Data & AI Challenge 2025
