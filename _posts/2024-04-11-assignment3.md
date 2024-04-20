---
title: "Assignment #3: Spatial Data"
date: 2024-04-11
categories:
  - assignment
tags:
  - spatial
  - data
toc: true
toc_label: "Contents"
toc_sticky: true
toc_icon: "bookmark"
---
# Assignment 3

## Introduction
In this assignment, we will be working with spatial data and representation of it. For this project, I decided to focus on the **"Brooklyn City and Business Directory for the year ending May 1, 1880"**. According to the description provided in [Archive.org](https://archive.org/details/1880BPL/page/n117/mode/2up), this site describes "Residential and business directory listings for the city of Brooklyn, NY in 1880. Includes Street and Avenue Directory as well as an appendix of government agencies and public services. Advertisements throughout, with index". Shortly, it is a business directory book that includes names, professions, adresses and even advertisements in the text. \
![business](/assets\images\business.png) \
An important point to note is that first, we will be working with the OCR that was already applied to the book. This means that the text is extracted directly from the image itself, and therefore might contain errors as the OCR is not perfect. \
Second, we will focus on exactly two pages of the book, as the size of the whole book makes it especially hard for ChatGPT to extract the information properly. More than anything, ChatGPT tends to do a poor job at dealing with faulty data, therefore we have chosen a page where we can extract the information without much issue.

## Processing of data and visualization

We will be working on the pages **95-96** of the directory. In this page, we have a list of multiple business owners, workers and various individuals. The common thing that unites all of them is the start of their surname, which is what the directory uses to index every person included in the book.
![directory](/assets\images\directory.png) \
For this assignment, we will work with a list of people that have surnames starting with **"BRE"**. This was a page specifically chosen to show a range of professions and addresses that we will see later.\
Once we extract the raw data from these pages, we will ask ChatGPT to generate a CSV file by organizing this information in columns and rows. The prompt is:
> (data)...\
 This is an OCR text extracted from "Brooklyn City and Business Directory for the year ending May 1, 1880". Please generate a csv file that will list the people featured in this data.

Initially, we had trouble generating the CSV file. As we mentioned, ChatGPT did not fare well dealing with data that might be in a different format or slightly "dirty". \

![ChatGPT](/assets\images\gpt.png)

Not only that, but ChatGPT decided to solve it by reducing the sample size. This, of course, was unacceptable and required a different prompt to generate the correct amount.

> Provide a CSV file with at least 50 rows. Do not create new data.

It is crucial to specify the last part, as ChatGPT tends to generate new data based on previous patterns. \
Finally, we were able to generate correctly a CSV file that could fit our needs. The file is included in the Github repository, under the assets folder. \
Once we have done this, we proceed to upload our file to Google Drive, where we will use Google Sheets to open the CSV file.\
![excel](/assets\images\sheets.png)

Now that we have our file in an editable form, we will use Geocode to generate the Latitude and Longitude of our addresses. First of all, we added **"Brooklyn,"** in front of every single address. Why did we do this? In our first try, Geocode did not provide accurate coordinates. For most data, it was unable to even pinpoint where it was. That is why we add Brooklyn in front of the address, so we are able to generate proper coordinates. 

![geo](/assets\images\geocode.png)

Geocode provided the coordinates for around 30 of the addresses, while 20 of them were unable to be found. However, the missing data comes from the OCR itself, therefore it would be unfair to blame Geocode for it. For example, we see addresses such as "h of Garnet". This is, logically, an invalid address. 

Once we finalize the geocoding, we proceed to [kepler.gl](https://kepler.gl).  
Kepler.gl is a powerful geospatial analytics and visualization tool that will allow us to see on an interactive map the coordinates that we previously generated.

![kepler](/assets\images\kepler.png) \
As we can see on the image, Kepler provided us an amazing visualization of the points generated.

## Conclusion and learnings
This project served as a great experience of learning how to visualize spatial data. It is specially hard to work with old addresses, even more when we are working with an inevitably unprecise OCR. It was surprising to see the amount of problems that surged starting from the data extraction process, all the way to the creation of the CSV file and the visualization of it. In future projects, I would love to work with a bigger dataset, maybe the whole book or entire categories. It would be a challenge to see how a bigger sample size changes our way to see this data. By working with OCR and geocoding, I was fascinated to see the power of spatial data. To be able to see the locations of houses that belonged to people hundreds of years ago was extremely profound and I will make sure to keep an eye on other spatial data projects around the world.

**READY FOR GRADING**
