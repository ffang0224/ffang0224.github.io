---
title: "Assignment #1: Cultural Heritage By the Numbers"
date: 2024-02-23
categories:
  - assignment
tags:
  - cultural
  - numbers
---

# Assignment #1: Cultural Heritage By the Numbers

This exercise focuses on the ways that the metadata obtainable from the Harvard Art Museum API can tell us something about historical and present world cultures, as well as the way they are represented in the contemporary Western museum. Today, we will dive deep into different methods of analyzing the data provided by the Harvard Art Museum and what relevant information about the background of the objects that might provide us.

## Part 1:

![HAM](/assets\images\HAM.png)
*Harvard Art Museum website*

![Gas Station](/assets\images\gasstation.jfif)

This is a photograph extracted from the Harvard Art Museum website. This work is called "Gas Station" by German artist Julian Faulhaber and it is one of the first images I got shown in the collections page of the website. In general, the website was highly intuitive and easy to navigate around. Users are able to filter works based on various characteristics of them.

![filters](/assets\images\filters.png)

Underneath the picture, we can find information about the people related to the work, the date and other relevant information that might be useful to the watcher. In specific, this section was interesting because it gives valuable insight on the work, the author and the background of it.

![Identification of image](/assets\images\info.png)

Diving into the ***All_Objects.csv*** file that we possess, we can see a list of all the objects included in the database of the HAM. In every column, we see the same information we previously saw in the website.

What is the need of having a comma-separated file if we already have the objects displayed on the HAM website? 

Individually, in comparison to the website, it seems like it is lacking the visual aspect that the website provides. However, the benefits of seeing the objects in a CSV comes from the ability to see the bigger picture, to analyze the cultures and objects in a broader (but still detailed) sense than one by one. 

![allcultures](/assets\images\cultures.png)

For example, if we wanted to see the descriptions and other metadata of all German culture objects to see certain patterns, similarities or constrasts, we would have to spend hours browsing the website and annotating all of that information. However, with the CSV, that problem is solved easily.

## Part 2:

Let's see more of what else CSV files have to offer.If we take a look into ***All_Cultures_information.csv*** and sort the list by object count, we will see the following information:

![AllCulturesInfo](/assets\images\allcultures.png)

At first glance, it might not signify much. However, from this list, we can see clearly the most prominent cultures in the museum. Specifically, we can note that many of the top cultures tend to be cultures that are or have been closely associated with the history of the United States of America. We can notice how British, Japanese, German objects are part of the most common cultures found in the museum's collection. With this, we can already guess how the fact that the museum is American affects the sample size of our data.

Now, we proceed to check the **Harvard_API_All_objects** notebook we will run in Posit Cloud. By connecting to the HAM API, we can scrape information from their collection, the same way it is presented in the CSV. Instead of organizing our data from the CSV, we will only reach out for the information we need. For this example, I selected the Argentinian culture, culture from my very own country of birth. By running the notebook, I obtained all objects that are catalogued as part of the Argentinian culture category and the amount of times people visited the page of that item.

> In case you interested about it, [here](/assets\misc\argobjects.txt) is the list of every object with the amount of views it has. 

Looking into it, it is interesting to see that one specific item has almost 10 times more views than the second most viewed page: "*Analogia 1*". This work consists of forty potatoes carefully placed in a gridded container that are all connected to electrodes that emit charges registered by the meter at the center. By checking on the HAM website and running a quick search on the Internet, we can see that the page for the object/installation was included in various articles and websites due to the interesting nature of the project. 

> In addition to being displayed in the [Museo Nacional de Bellas Artes](https://www.bellasartes.gob.ar/) in Buenos Aires, the name hides an extremely interesting play of words: *Analogia* is the spanish word for analogy, but also contains the word *analog*, which is the motive behind the electric theme of the installation.

![analogia](/assets\images\analogia1.png)
*"Analogia 1" by Victor Grippo*

What if we check the other way around? As for the least viewed items, very little information can be deducted from them. However, one common thing between all of them is that many of them are from the same author, Máximo Gonzalez. Maybe his style is not very appealing to the general public, but the main point would probably be the fact that despite being catalogued as Argentinian culture, the art depicts things from Mexico. One thing is for sure, this artist did not prove to be especially popular.

![Puebla](/assets\images\puebla.png)
*"Magazine stand: City Center of Puebla" by Maximo Gonzalez*

## Part 3:

This time, instead of cataloguing our information in a CSV, we will utilize the information to create a wordcloud. Why should we do this? Truth is, a lot of information about a certain culture can be inferred from the most common words of their works. Let's take for example the British culture category. Running the notebook to create a wordcloud outputs this:

![British Wordcloud](/assets\images\britishWordCloud.png)

From this wordcloud, we can see various points of interest. First of all, "*Untitled*" seems to be one of the most common words in the collection. Logically, hundreds of items are untitled due to the long history United States has with the British empire. Aside from that, we can see various elements that correlate perfectly with our perception of British history: Castle, Figure, Man, Lady, etc. 

One important thing we have to note is the importance of stopwords. Words such as "the", "from", "as", and many others are very common words utilized in the English Language. Therefore, finding them does not provide us with any relevant information about the culture itself. Rather, they are minimizing the impact other words have. 

Following, we have the words for the Greek and Japanese cultures:

![Greek](/assets\images\greece.png)
![Japan](/assets\images\japan.png)

> Here we can see how the Japanese diagram contains NAN in the middle. Due to the difficulties translating from Japanese to English, it is common for items to be untitled or have a NAN name, which means no name was applied. 

Not only the common words are useful in this case. The accession date tell also a story and a background behind it. Here is a diagram of the amount of objects accessed throughout the years:

![Accession](/assets\images\accessionplot.png)

This diagram, although simple at first sight, can show us when the Harvard Art Museum, an American museum, obtained various objects of a certain culture. Due to the history of the United States, American museums tend to possess various items from countries they have been related to, either in alliance or as enemies. Therefore, we can note, for instance, the prominent Japanese presence in the collection. 

For example, looking into the Japanese accession years, we can see a very noticeable peak around 1940. If we look back into history, we will see that Japan officially entered World War II on September 22, 1940 with the invasion of French Indochina. Interestingly enough a significant peak is seen on the dates that match the World War II. Although it is not enough to obtain a conclusion, it is incredibly interesting to see how this information can tell us a whole story without explicitly stating it.

## Extra part + Conclusion

Finally, using the **objects_with_places** notebook, we are able to create the following map based on items from the German culture:

![Germany](/assets\images\germanymap.png)

This map plots the origin place for each of the items in the collection. Interestingly enough, although a big part of them are originated in Germany, multiple objects are catalogued as items coming from the East and West Coast of the US. Even though it is not a confirmation, we can deduce that this disparity comes from the big inmigrant population residing in both coasts of the country. 

In conclusion, this project was a very interesting insight into different methods of scraping data from APIs such as the Harvard Art Museum API. Not only that, but we also have learned how metadata can provide huge amounts of context and information that can be valuable for us to further explore and understand the background of each culture, each object featured in the collection. The date in which it was accessed, the author and the place where it was originated are just examples of how important metadata can be in the context of big clusters of data. We will further explore bigger amounts, formats and varieties of data, so proper use of the skills learned today will be key in the future. I hope this was an enjoyable read and I am excited for what future projects await us. 

***READY FOR GRADING***