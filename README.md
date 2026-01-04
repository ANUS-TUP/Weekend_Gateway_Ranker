🌄 Weekend Getaway Ranker – Data Engineering Project
📌 Project Overview

The Weekend Getaway Ranker is a rule-based travel recommendation engine built using Python and Pandas.
Given a source city, the system ranks the top weekend destinations in India based on:

Distance (approximate)

Google review rating

Popularity (number of reviews)

The project uses India’s Must-See Places dataset and demonstrates core data engineering and ranking logic.

🎯 Problem Statement

Data Engineering: Weekend Getaway Ranker

Build a recommendation engine for local travel based on the Travel Dataset (India’s Must-See Places).

Task

Create an algorithm that:

Takes a Source City as input

Ranks top weekend destinations

Uses distance, rating, and popularity as ranking factors

Technologies

Python

Pandas

Submission Requirements

Python / Jupyter code

requirements.txt

Sample output for three different cities

🛠 Technologies Used

Python 3.x

Pandas

NumPy

Jupyter Notebook

📂 Project Structure
Weekend-Getaway-Ranker/
│
├── Weekend_gateway_ranker.ipynb   # Main notebook
├── Top Indian Places to Visit.csv # Dataset
├── requirements.txt
└── README.md

🔍 Dataset Description

The dataset contains information about tourist places in India, including:

City

State

Place name

Google review rating

Number of Google reviews (in lakhs)

Best time to visit

⚠️ Note:
The dataset does not include latitude/longitude, so approximate city-to-city distances are used.

🧠 Algorithm Explanation (Step-by-Step)

Load Dataset

Read CSV file using Pandas

Standardize column names

Data Cleaning

Remove rows with missing city, state, rating, or popularity

Distance Approximation

Use predefined city-to-city distance mapping

Assign default distance if mapping is unavailable

Feature Normalization

Normalize rating, popularity, and distance

Scoring Formula

score = (0.5 × rating) + (0.3 × popularity) − (0.2 × distance)


Ranking

Sort destinations by score

Return top N weekend getaways

⚙️ Installation:
1️⃣ Clone the Repository
git clone https://github.com/ANUS-TUP/weekend-getaway-ranker.git
cd weekend-getaway-ranker

2️⃣ Create Virtual Environment (Optional but Recommended)
python -m venv venv
source venv/bin/activate      # Linux / Mac
venv\Scripts\activate         # Windows

3️⃣ Install Dependencies
pip install -r requirements.txt

▶️ Execution (How to Run Locally)
1️⃣ Start Jupyter Notebook
jupyter notebook

2️⃣ Open the Notebook
Weekend_gateway_ranker.ipynb

3️⃣ Run All Cells

Click Kernel → Restart & Run All

▶️ How to Use the Recommendation Function

Example:

recommend_weekend_getaways(df, source_city="Delhi", top_n=5)

📊 Sample Output:
Source City: Delhi
Agra        | Uttar Pradesh | 233 km | 4.6 | 8.5 | 0.82
Jaipur     | Rajasthan     | 281 km | 4.5 | 7.9 | 0.79
Mathura    | Uttar Pradesh | 183 km | 4.4 | 6.8 | 0.76

Source City: Bangalore
Mysore     | Karnataka | 145 km | 4.7 | 9.2 | 0.88
Coorg      | Karnataka | 252 km | 4.6 | 8.1 | 0.84
Ooty       | Tamil Nadu| 270 km | 4.5 | 7.8 | 0.81

Source City: Mumbai
Pune       | Maharashtra | 149 km | 4.6 | 8.9 | 0.86
Lonavala   | Maharashtra | 83 km  | 4.5 | 7.4 | 0.83

📦 requirements.txt:
pandas
numpy

🚀 Future Enhancements:

Integrate latitude/longitude for real distance calculation

Add budget and travel time filters

Convert notebook to a Python script

Deploy as a web application

🧠 Learning Outcomes:

Data preprocessing using Pandas

Feature normalization techniques

Rule-based recommendation systems

End-to-end data engineering workflow

👨‍💻 Author-Anustup Das
