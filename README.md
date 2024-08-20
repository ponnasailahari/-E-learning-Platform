# Elearning-website

--This is an e-learning website prototype. This website was created as a final deliverable for our internship. Due to the sensitive nature of the data, actual code and datasets cannot be uploaded. It consists of features such as Chatbot, Recommendation System, Search Engine, Profile and Course Management. The user is required to create a profile which consists of details such as interests, previous courses and educational information. Based on these details, courses are recommended to the user. The user can search for specific courses, check course details and can use the conversational chatbot interface to ask questions about the website.

Explanation:

The website was an integration of our 3 individual projects: Chatbot, Smart Search, Recommendation System.

# A. Smart Search

--A Search Engine that provided the features of Auto-Completion of Search queries, Fuzzy-String matching and filtering of results based on other user’s choices.
Search would enable learner to find a specific course among the entire list of courses based on Course Id, Course Title, Department, etc.
Returning results for search query is done based on Levenshtein Distance to calculate distances between sequences. This checks similarity between entered query and actual course title from the entire list.
The results are ranked and sorted based on the Clickstream Analysis to show courses with highest preference above other courses.
Smart Search ensures no null results are returned for any query.
The engine is able to understand spelling errors and is able to approximate to most similar entries in the data.
Auto-Complete to suggest queries on typed individual characters is implemented to reduce learner effort to type out complicated course titles and to avoid spelling mistakes.

# B. Recommendation System

--A Recommendation System was to be developed that would recommend learners with courses based on their interests, overall profile, similarity to other courses, etc.
Recommendation System would aggregate all attributes of a course such as Course Title, Course Description, Languages, Domains, etc.
Recommendation based on Related Courses and User Profile utilizes Scikit learn Feature extraction CountVectorizer to convert the data into a sparse matrix and then uses cosine similarity measure to find the next course most similar to the given course.
Recommendation based on Collaborative Filtering utilizes the surprise open source library to implement the SVD++ collaborative filtering algorithm which returns the courses you are most likely to take based on what you and people similar to you have rated.

# C. Chatbot

This project involved the development of a Chatbot for customer service needs such as real-time querying and automated answering.
Chatbot acts as atrained assistant that can provide learners with answers and guidance.
There was a need for Live Natural Processing in the Chatbot.
A (8x8) neural network is trained based on the possible conversation users might have with chatbot such as questions based on course type and course details.
Chatbot uses Lancaster Stemmer and Natural Language Toolkit(nltk), python libraries to perform NLP operation to better understand the context.
Tensorflow, tflearn are used for building the neural network.
