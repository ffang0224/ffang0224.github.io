---
title: "Love Data Week: Tableau Workshop"
date: 2024-02-19
categories:
  - assignment
tags:
  - tableau
  - data
---

# Extra credit event

## Date, time and location of event: 
### Wed Feb 7, 2024 9pm – 11pm GST (Remote)

## Name of event: 
### Data Visualization with Tableau (Workshop)

## Description
On February 7th, I attended a Tableau Workshop in the context of the Love Data Week. This workshop is part of the NYU Library classes. They offer multiple events, workshops and activities related to various fields including data science, data visualization, academic resources and other categories.

## What is Tableau?
For those who do not know, **Tableau** is a popular interactive data visualization tool that provides us with multiple chart formats and mapping functions.

This is a widely used software in every field that applies data visualization. In my case, I decided to utilize the Tableau Public version of this software. The key capacities are fundamentally the same, but the other versions that NYU provides access to required a prior registration and verification process.

This is an example taken from a sample provided in class, which I inputted into Tableau:
![example1](/assets\images\TableauExample1.png)

At first glance, it might look very similar to a Microsoft Excel file. Well, that is because the data is extracted from an Excel FIle. However, the capacities of Tableau go beyond that. One of the best things that we can do in Tableau is representing multiples types of data. In general, many softwares are able to process text data easily. Also, numbers tend to be easy to represent too. Actually, Excel and Sheets can definitely show that. But what happens to other types of data? More importantly, what about the context of our data?

## Data in context
Data is nothing if we put do not add context to it. Let's ask ourselves one question (This is a rethoric quesiton that was presented in class): Is a 100 a lot?
If we were to say **100 diamonds**, that would sound like a big number. After all, diamonds are rare. What about **100 rocks**? That doesn't sound as exciting, right? That is exactly what happens to data. The number, the text, the information itself is irrelevant if we don't pair it with its appropiate context.

From now one, for this post, I will be using an Excel Spreadsheet that contains multiple [Olympic medalists](/assets/spreadsheets/OlympicAthletes.xlsx). 

This is what the raw data looks like when we look at the country field:

![example4](/assets\images\TableauExample4.png)

Very pretty and organized. However, as someone who is not especially proficient at locating countries in the map, I tend to not take too much value into this information. 

Here is what Tableau will automatically show us when we select the country field:


![example2](/assets\images\TableauExample2.png)

Here we can clearly see all the countries that are represented in medalist spreadsheet. This way, not only we can notice certain tendencies and patterns, but also we can easily identify multiple countries that did not win a single medal (or are not figured in the spreadsheet).

## Data visualization
Context matters, and the way we show data too. Personally, after this workshop, I learned how important it is to present information in the correct format. Even though spreadsheets are powerful, they often present a complicated solution to a simple problem. More than anything, our representation is not only our way to portray the solution, but also our way of showing how we are interpreting the problem. 

Here we will show an easy example of what I mean. In the following picture, we can see a list of every single medal winner included in our data source. This is a simple horizontal bar graph with each bar representing the age of the athelete. This is a simplistic and elegant way of portraying the ages. In this case, this graph could be the answer to a question such as "Who is the oldest/youngest athlete?". It is very important, because the main component here that our human eye will perceive is the length of the bar. We do not put too much emphasis on how old they are, nor do we have to remember who was the oldest/youngest so far: all we care about is the maximum and minimum age, which we will easily recognize by finding the longest/shortest bar.

![example5](/assets\images\TableauExample5.png)

What about this graph? This graph is a bar graph that displays the age of the athletes, but this time divided by country. 

![example6](/assets\images\TableauExample6.png)

The question this time could be "Who is the oldest/youngest athlete **in X country**?". In this graph, we will identify it easily by seeing the graph and doing the same thing we did previously. 

## Learnings, application to course content and future projects
In conclusion, I was very satisfied with what I learned in this workshop. Not only I learned how to utilize one of the, if not the most popular software in the world of data visualization, but also learned key concepts regarding the context and representation of data. These are topics that we have discussed previously in class, but it was gratifying to see them applied in the real world (or at least, a simulation of it). I personally link these concepts to the assignment 1, where we will be extracting information from a public API and graphing the data in word clouds and tables. I think Tableau could be paired with tools such as the notebooks provided in the course in order to, for example, generate a bar graph of every country's amount of objects in the museum. As a student interested in Data Science, I will definitely utilize this software in future projects such as capstone and my career, so I am extremely glad I have taken this workshop. 

## Links

- [Olympic Atheletes Spreadsheet](/assets\spreadsheets\OlympicAthletes.xlsx)
- [NYU Library Guide for Tableau](https://guides.nyu.edu/viz/tableau)
- [Slides for the workshop](https://docs.google.com/presentation/d/18ec2H10MVbP2E0Exe-QGKDZWBzjjfPxjP-A-kJAdEms/edit?usp=sharing)
- [Attendance Confirmation](/assets\images\confirmation.png)


