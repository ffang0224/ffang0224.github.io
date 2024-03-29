---
title: "Assignment #2: Exploring Textual Data from a Custom Corpus"
date: 2024-03-21
categories:
  - assignment
tags:
  - text
  - data
---

- [Introduction](#introduction)
- [Analysis](#analysis)
- [Conclusion and Learnings](#conclusion-and-learnings)

## Introduction

This assignment will focus on the works of writer Arthur Conan Doyle, commonly known for creating the character Sherlock Holmes, arguably the most popular fictional detective of all time. Specifically, we will be diving into the textual characteristics of 3 of his most known works, identifying the differences, the context, and the information this data brings to our knowledge of the author. 

![Arthur Conan Doyle](/assets\images\arthurconandoyle.png)

First and foremost, we will present the 3 texts we will be working with throughout the assignment, all of them extracted from [Project Gutemberg](https://www.gutenberg.org/):
- ***A Study in Scarlet***: A novel published in 1887 that marks the first appearance of Sherlock Holmes and Dr. Watson. The first full-length novel that included the detective duo initially attracted very little public interest but later on became one of the most popular Sherlock Holmes stories. 
- ***The Adventures of Sherlock Holmes***: A collection of short stories published in 1892.  It contains the earliest short stories featuring the detective Sherlock Holmes, earning immense popularity for both Sherlock Holmes and Dr. Watson.
- ***The Memoirs of Sherlock Holmes***: A collection of short stories first published late in 1893. Initially supposed to be the last Sherlock Holmes story, this book presents 12 stories that ultimately end with the "death" of Sherlock Holmes.

### Rationale:
Arthur Conan Doyle is one of the, if not the most popular writers in the history of crime fiction. His works transcended language and race, and his character, *Sherlock Holmes*, went on to become the most famous (fictional or not) detective of all time.\
One of the biggest motives behind choosing his works as study subjects is the variety of content he presented throughout his career. In 1891, Doyle intended to kill *Sherlock Holmes*, so he raised his price to a level intended to discourage the publishers that demanding more stories. However,  he later realized they were willing to pay even the large sums he asked, forcing him to create multiple plot twists that made *Sherlock Holmes* stories a rollercoaster of events.

![scarlet](/assets\images\scarlet.png)\
*A Study in Scarlet, 1887* 

The reason behind choosing these 3 works is the similarity, yet disparity they present. First of all, they are not presented in the same format. Although ***"A Study in Scarlet*** is a full-length novel, the other 2 works are a series of short stories.\
In addition, it is important to note the dates on which Arthur Conan Doyle published the stories. After ***"A Study in Scarlet***, *Sherlock Holmes* received a boost in popularity that was further accentuated with the publishing of ***The Adventures of Sherlock Holmes***.\
Therefore, we will note certain differences in Doyle's writing style, mostly due to the sudden increase in audience and the fact that he intended to kill the character of *Sherlock Holmes* in ***The Memoirs of Sherlock Holmes***, a very sensitive plot move that forced him to focus on the character development of the detective. Although he did so, due to public backlash, he ultimately ended up reviving the character in further works.

## Analysis
In this part, we worked with **Voyant Tools** in order to textually analyze the works of Arthur Conan Doyle. This tool provided us with valuable information that would otherwise not be available to the human eye. Presented here, we see word clouds generated by Voyant Tools for each of the works.

![adventures](/assets\images\adventures.png)\
*"The Adventures of Sherlock Holmes"*

![study](/assets\images\study.png)\
*"A Study in Scarlet"*

![memoir](/assets\images\memoir.png)\
*"The Memoirs of Sherlock Holmes"*
---

![all texts](/assets\images\alltexts.png)

This **word cloud** we see here presents the 95 most common terms throughout the 3 works. We can clearly see various common words that at first glance might not provide much useful information, but once we put them in context they are more meaningful than they look.

> To analyze this properly, we will ignore words such as "gutenberg", "project", "just", "quite", etc...\
These are just words that appear either due to the fact that we obtained the raw text from Project Gutemberg or because they are part of basic English grammar.

For example, take the word **"room"**. One might assume that this is just due to the fact that it is a daily-use English word. However, if we think about it deeply, it would not be utilized with such a frequency in normal sentences.

![room](/assets\images\room.png)\
*Word count for the word "room" throughout the entire corpus*

If we look at the word occurrence for the word "room" and its variations ("rooms", mostly), we will see that the word is mentioned a total of **474** times, a huge amount for such a specific word.\
Once we link it with the context of the works, it all makes sense: *Sherlock Holmes*, being a detective, often has to examine the room and analyze the hints that will lead him to the suspect. Logically, this word will appear very often if we additionally consider the root behind the name of the first novel: ***"A Study in Scarlet"***.\
The book's title derives from a speech given by Holmes, a consulting detective, to his friend and chronicler Watson on the nature of his work, in which he describes the story's murder investigation as his **"study in scarlet"** inside the room. Similarly to this, we can also find multiple words that fit the detective genre, such as "case", "police" and "inspector".

<iframe style='width: 509px; height: 366px;' src='https://voyant-tools.org/tool/CorpusTerms/?lang=en&corpus=d2010ebf841098c77408308469ac183e'></iframe>\

*Word count of terms in the corpus*

---

Looking through a more general perspective, we can derive some information from other tools in **Voyant Tools**. For example, the place where find the occurrences of certain words can help us determine some information. Similarly to the Google Books Ngram Viewer (Week 4), we can check on the frequencies of any set of search strings in the corpus.

<iframe style='width: 509px; height: 366px;' src='https://voyant-tools.org/tool/MicroSearch/?lang=en&query=sherlock*&panels=corpusterms%2Creader%2Ctrends%2Csummary%2Ccontexts&corpus=d2010ebf841098c77408308469ac183e'></iframe>

*Occurrences of the word "Holmes" in "A Study in Scarlet"*

*Sherlock Holmes* stories tell a criminal fiction tale that usually involves a crime, an investigation, and finally, a resolution by the detective. ***"A Study in Scarlet"*** is no exception to this pattern.

 We can see that the word **"Holmes"** is very mentioned in the **first half**, decays entering the **start of the second half** and **finishes** towards the end with a few stellar apparitions. This is due to the fact that the second half usually includes the crime itself, in which our detective does not take part.\
Holmes only appears to resolve the conflict, to capture the criminal in the most essential *Sherlock Holmes* style, with little collaboration with the police and taking credit for it.

Additionally, we can also see the tendency of certain topics, words, and contexts inside the works themselves. For example, let's take a look at the word **"watson"**.

![watson](/assets\images\watson.png)\
*In order left to right: "The Adventures of Sherlock Holmes", "A Study in Scarlet" and "The Memoirs of Sherlock Holmes"*

We can see a clear dip in the occurrence of the word in ***"A Study in Scarlet"***.

> Note: This diagram depicts the *relative* occurrence of the word, which compares it to the total amount of words in the document. Therefore, the length of each document does not pose a significant change. 

This is due to the fact that Dr. Watson is only introduced in the first novel, and obtains a much more relevant role in the stories that follow. Initially, this character is nothing more than just a loyal sidekick, and his life is not documented/explained in such detail in ***"A Study in Scarlet"*** compared to the other works.

## Conclusion and Learnings

In conclusion, analyzing books through the textual information provided is a valuable tool that can complement the background we have. It can help us determine patterns, visualize occurrences of phrases and words, and even provide surprising statistics about the texts.

By looking at the text through these tools, we can notice things that are impossible/very hard to remark without computer-assisted analysis. For example, I was surprised to see that the word "Watson" was not as popular as others. However, it makes more sense once we consider the fact that the works we included do not delve deep into the life of Dr. Watson, especially ***"A Study in Scarlet"***. Noticing this fact would have taken hours, days, and maybe weeks to analyze the text meticulously by hand, but with the digital format and the tools provided, we did a quick inference in a matter of minutes.

<iframe style='width: 100%; height: 800px;' src='https://voyant-tools.org/?lang=en&panels=cirrus%2Creader%2Cmicrosearch%2Csummary%2Ccontexts&corpus=d2010ebf841098c77408308469ac183e'></iframe>

Although we were not able to see exactly the difference in Doyle's writing style that I expected to see, it was highly valuable to see the trends of each word and especially, the number of appearances of each word throughout the corpus. If we recall on Johanna Drucker's post, we will see that the visualization of the data itself might be equally or even more important than the raw information itself. Instead, sometimes, the biggest challenge resides in producing "graphics that are appropiate to the research task and communication of arguments" (Drucker:100). I personally consider that this tool will be essential any time I analyze texts and works from any author and even in multiple languages. I hope I can keep getting familiarized with the concept of textual analysis and I wish to apply it in further projects.

## References

- [A Study In Scarlet Wikipedia](https://en.wikipedia.org/wiki/A_Study_in_Scarlet)
- [The Memoirs of Sherlock Holmes Wikipedia](https://en.wikipedia.org/wiki/The_Memoirs_of_Sherlock_Holmes)
- [The Adventures of Sherlock Holmes Wikipedia](https://en.wikipedia.org/wiki/The_Adventures_of_Sherlock_Holmes)
- [Arthur Conan Doyle Wikipedia](https://en.wikipedia.org/wiki/Arthur_Conan_Doyle)
- [Arthur Conan Doyle Biography Britannica](https://www.britannica.com/biography/Arthur-Conan-Doyle)

- [Voyant Tools Documentation](https://voyant-tools.org/docs/#!/guide)
- [Project Gutenberg](https://www.gutenberg.org/)
- Accardo, Pasquale J. (1987). Diagnosis and Detection: Medical Iconography of Sherlock Holmes. Madison, NJ: Fairleigh Dickinson University Press. ISBN 0-517-50291-7.
- Harrison, Michael (1973). The World of Sherlock Holmes. London: Frederick Muller Ltd.
- Shaw, John B. (1995). Encyclopedia of Sherlock Holmes: A Complete Guide to the World of the Great Detective. London: Pavilion Books. ISBN 1-85793-502-0.
- Drucker, J. (2021). The Digital Humanities Coursebook: An Introduction to Digital Methods for Research and Scholarship (1st ed.). Routledge. https://doi.org/10.4324/9781003106531
- Ricaurte, Paola, et al. Global Debates in the Digital Humanities. University of Minnesota Press, 2022. Project MUSE muse.jhu.edu/book/100081. 


**READY FOR GRADING**