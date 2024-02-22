# my-new-project
Building AI course project
<!-- This is the markdown template for the final project of the Building AI course, 
created by Reaktor Innovations and University of Helsinki. 
Copy the template, paste it to your GitHub README and edit! -->

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
Once you upload an image to your repository, you can link link to it like this (replace the URL with file path, if you've uploaded an image to Github.)
![Cat](https://upload.wikimedia.org/wikipedia/commons/5/5e/Sleeping_cat_on_her_back.jpg)

If you need to resize images, you have to use an HTML tag, like this:
<img src="https://upload.wikimedia.org/wikipedia/commons/5/5e/Sleeping_cat_on_her_back.jpg" width="300">

This is how you create code examples:
```
def main():
   countries = ['Denmark', 'Finland', 'Iceland', 'Norway', 'Sweden']
   pop = [5615000, 5439000, 324000, 5080000, 9609000]   # not actually needed in this exercise...
   fishers = [1891, 2652, 3800, 11611, 1757]

   totPop = sum(pop)
   totFish = sum(fishers)

   # write your solution here

   for i in range(len(countries)):
      print("%s %.2f%%" % (countries[i], 100.0))    # current just prints 100%

main()
```


## Data sources and AI methods
Data sources include user profiles, viewing history, ratings, and metadata from Netflix. AI methods encompass collaborative filtering, content-based filtering, and hybrid recommendation systems. Natural language processing (NLP) techniques may be utilized to understand user preferences and show descriptions.
## Challenges

Challenges include addressing the cold start problem for new users with limited viewing history, ensuring diversity in recommendations to avoid filter bubbles, and maintaining user privacy by securely handling sensitive data.

## What next?

Future enhancements could involve incorporating real-time user feedback to continuously improve recommendations, integrating social features for sharing and discussing series with friends, and expanding to recommend content from other streaming platforms. Collaboration with Netflix and access to their API would facilitate more accurate and comprehensive recommendations. 


## Acknowledgments

This project draws inspiration from Netflix's recommendation system and research in personalized content recommendation algorithms.
