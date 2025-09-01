 PySpark projects:

 Movie Recommendation System

Uses MovieLens 100K
 dataset.

Spark Projects: Degrees of Separation & Movie Recommendations
Two powerful Apache Spark applications demonstrating graph processing and collaborative filtering for recommendations.

Built using PySpark, these projects analyze large-scale datasets to solve real-world problems:

Find the shortest path between fictional characters (BFS in Spark)
Recommend similar movies using cosine similarity
 Project 1: Degrees of Separation (Marvel Superheroes)
 Problem
How many degrees of separation are there between two Marvel characters based on comic book co-appearances?

This project implements a Breadth-First Search (BFS) algorithm on a graph of superheroes to find the shortest path from a starting character to a target.

 Dataset
marvel-graph.txt: A tab-separated file where:
First column = Hero ID
Subsequent columns = IDs of heroes they appeared with
Inspired by Marvel Comics data from the Stanford Network Analysis Project (SNAP) 

 How It Works
Start: Character ID 5306 (e.g., Loki)
Target: Character ID 14 (e.g., Spider-Man)
Uses BFS iterations to propagate through the graph
Employs a Spark accumulator to detect when the target is found
Nodes are colored:
GRAY: Being explored
BLACK: Already processed
WHITE: Not yet discovered
Key Spark Concepts Used
flatMap() for spreading the search
reduceByKey() to merge duplicate nodes
Accumulators for global counters
In-memory distributed graph traversal

 Project 2: Movie Recommendation System
 Problem
Given a movie, recommend other movies that are most similar in terms of user ratings.

Uses cosine similarity to compute how closely two movies are rated across users.

 Dataset
ml-100k/u.data: User ratings (user ID, movie ID, rating, timestamp)
ml-100k/u.item: Movie metadata (ID, title, genre, etc.)
From the classic MovieLens 100K dataset
