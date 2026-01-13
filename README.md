# Building Social Network Recommendations from Raw Data Using Python

## Overview
This project demonstrates how core social network recommendation features
can be built **from raw data using pure Python**.

The focus is on implementing recommendation logic from first principles,
without using libraries such as pandas, NumPy, or machine learning frameworks.

The system replicates two common social platform features:
- People You May Know
- Pages You Might Like

---

## Project Objectives
- Clean and structure raw social network data
- Build friend recommendations using graph traversal
- Build page recommendations using shared interests
- Validate logic on both small and large datasets

---

## Dataset Description
The dataset represents a simplified social network and contains:
- Users with unique IDs
- Friend relationships between users
- Pages liked by users

All data is stored and processed in JSON format.

---

## Recommendation Logic

### People You May Know
- Identifies friends-of-friends for a given user
- Excludes existing connections
- Ranks potential recommendations by number of mutual friends

This approach is based on basic social graph traversal.

### Pages You Might Like
- Collects pages liked by a user’s friends
- Excludes pages already liked by the user
- Ranks pages based on frequency within the user’s network

---

## Project Structure
```yaml
Building_Social_Network_Recommendations_from_Raw_Data_Using_Python/
│
├── data/
│   ├── data2.json                     # Row social network data
│   ├── data1.json                     # Raw social network data
│   ├── cleaned_codebook_data.json    # Cleaned and structured dataset
│   └── massive_data.json             # Large dataset for scalability testing
│
├── Building_Social_Network_Recommendations_from_Raw_Data_Using_Python.ipynb
│                                      # End-to-end implementation:
│                                      # data cleaning + recommendations
│
├── PROJECT_REPORT.md                  # Detailed technical explanation
└── README.md     