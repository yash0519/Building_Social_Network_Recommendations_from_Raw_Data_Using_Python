# Project Report  
## Building Social Network Recommendations from Raw Data Using Python

---

## 1. Introduction
Recommendation systems are a fundamental part of modern social networks.
They help users discover new connections and relevant content.

This project focuses on building such recommendation features **from raw
social network data using pure Python**, prioritizing logic and data
structures over external libraries.

---

## 2. Problem Statement
Given raw social network data containing:
- Users
- Friend relationships
- Page interests

The goals of this project are to:
1. Clean and structure the raw data
2. Recommend new people a user may know
3. Recommend pages a user may be interested in

---

## 3. Data Cleaning and Preparation
The raw dataset contained multiple inconsistencies, including:
- Missing or empty user names
- Duplicate friend entries
- Inactive users with no relationships
- Duplicate page records

The cleaning process involved:
- Removing users with missing names
- Deduplicating friend lists
- Removing inactive users
- Deduplicating pages using unique IDs

The cleaned data was stored in JSON format for further analysis.

---

## 4. People You May Know Recommendation
This feature is implemented using social graph traversal techniques.

Steps involved:
1. Identify the target user’s direct friends
2. Find friends-of-friends
3. Exclude users already connected to the target user
4. Rank potential recommendations based on mutual friend count

This approach mirrors basic friend recommendation logic used in social
network platforms.

---

## 5. Pages You Might Like Recommendation
Page recommendations are generated using interest overlap within a user’s
social network.

Steps involved:
1. Collect pages liked by the user’s friends
2. Exclude pages already liked by the user
3. Count the frequency of remaining pages
4. Recommend the most relevant pages

---

## 6. Scalability Testing
The same recommendation logic was tested on a larger dataset to ensure
correctness and reasonable performance without relying on external libraries.

This validated that the approach scales logically with increased data size.

---

## 7. Limitations
- The system uses rule-based logic rather than machine learning
- Performance is limited by in-memory processing
- No real-time or streaming updates are implemented

These limitations are intentional to keep the focus on fundamentals.

---

## 8. Conclusion
This project demonstrates the ability to:
- Work directly with raw structured data
- Implement recommendation systems from first principles
- Apply graph-based reasoning using Python

It reflects strong foundational skills relevant to Python and data-focused
roles.
