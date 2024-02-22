# my-new-project
Building AI course project
<!-- This is the markdown template for the final project of the Building AI course, 
created by Reaktor Innovations and University of Helsinki. 

# Project Title

Final project for the Building AI course

## Summary

This AI project aims to recommend Netflix series to users based on their preferences and viewing history, enhancing their entertainment experience and helping them discover new content tailored to their interests.


## Background

With the vast amount of content available on Netflix, users often struggle to find shows that match their tastes. This project addresses the common problem of decision fatigue and the overwhelming choices users face when selecting what to watch. By leveraging AI algorithms, personalized recommendations can be generated, increasing user satisfaction and engagement.

- Decision fatigue in selecting Netflix series
- Overwhelming choices leading to indecision
- Personalized recommendations improving user satisfaction

## How is it used?

Users provide input regarding their preferences, such as genres they enjoy, favorite shows, or ratings of previously watched series. The AI algorithms analyze this data along with Netflix's extensive content library to generate tailored recommendations. Users can explore suggested series and choose the ones that interest them.

Images will make your README look nice!

Code examples:
import pandas as pd
from sklearn.metrics.pairwise import cosine_similarity

ratings_data = {
    'User': ['User1', 'User2', 'User3', 'User4'],
    'Stranger Things': [5, 4, 0, 4],
    'The Crown': [4, 5, 3, 0],
    'Breaking Bad': [0, 4, 5, 5],
    'Narcos': [3, 0, 4, 3],
    # Add more series and ratings as needed
}

ratings_df = pd.DataFrame(ratings_data)
cosine_sim = cosine_similarity(ratings_df.drop('User', axis=1))

def get_recommendations(user):
    user_index = ratings_df[ratings_df['User'] == user].index[0]
    sim_scores = list(enumerate(cosine_sim[user_index]))
    sim_scores = sorted(sim_scores, key=lambda x: x[1], reverse=True)
    sim_scores = sim_scores[1:]  # Exclude self
    similar_users = [i[0] for i in sim_scores]

    recommendations = []
    for user_index in similar_users:
        for series, rating in ratings_df.drop('User', axis=1).iloc[user_index].items():
            if rating > 3 and ratings_df.iloc[user_index][series] == 0:
                recommendations.append(series)
    return recommendations[:5]  # Return top 5 recommendations

user = 'User1'
recommended_series = get_recommendations(user)
print(f"Recommended series for {user}: {recommended_series}")



## Data sources and AI methods
Data sources include user profiles, viewing history, ratings, and metadata from Netflix. AI methods encompass collaborative filtering, content-based filtering, and hybrid recommendation systems. Natural language processing (NLP) techniques may be utilized to understand user preferences and show descriptions.
## Challenges

Challenges include addressing the cold start problem for new users with limited viewing history, ensuring diversity in recommendations to avoid filter bubbles, and maintaining user privacy by securely handling sensitive data.

## What next?

Future enhancements could involve incorporating real-time user feedback to continuously improve recommendations, integrating social features for sharing and discussing series with friends, and expanding to recommend content from other streaming platforms. Collaboration with Netflix and access to their API would facilitate more accurate and comprehensive recommendations. 


## Acknowledgments

This project draws inspiration from Netflix's recommendation system and research in personalized content recommendation algorithms.
