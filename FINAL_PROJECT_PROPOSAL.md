## Final Project Overview

This document provides an overview of the group members, tools, and data documentation for the Final Project

#######################

## Members

Jawaid Hakim 

## Introduction - NLP, NLU, NLG

NLP (Natural Language Processing), NLU (Natural Language Understanding), and NLG (Natural Language Generation) are important subtopics of Machine 
Learning. 

NLP it involves programming computers to process massive volumes of language data. It involves numerous tasks that break down natural language into 
smaller elements in order to understand the relationships between those elements and how they work together. NLP focuses largely on converting text to 
structured data. It does this through the identification of named entities (a process called named entity recognition) and identification of word 
patterns, using methods like tokenization, stemming, and lemmatization, which examine the root forms of words.

NLU is a subset of natural language processing, which uses syntactic and semantic analysis of text and speech to determine the meaning of a sentence. 
One of the primary goals of NLU is to teach machines how to interpret and understand language inputted by humans. It aims to teach computers what a 
body of text or spoken speech means. NLU leverages AI algorithms to recognize attributes of language such as sentiment, semantics, context, and intent. 
It enables computers to understand the subtleties and variations of language.

NLG is also a subset of NLP and is concerned with enabling machines to not just process and understand text but to generate text. While NLUg focuses on 
computer reading comprehension, NLG enables computers to write. NLG is the process of producing a human language text response based on some data input

## Project Goal

Recent advancements in NLP, most notable the NLG capabilities of Large Language Models (LLM) like ChatGPT, have taken the public imagination by storm. In this
project we will explore the following:

- Create a NLP classfier to classify product reviews as either real (created by an actual user of the product) or fake (created by a BOT or fake human 
reviewer). For this I will use (fake reviews dataset)[https://osf.io/3vds7]
- 

## Tools

We are using **Slack** and **Zoom** as the primary collaboration tools. **Github** is used as the repository for all artifacts (R code, SQL scripts, ER diagrams, etc.). For ease of sharing data, we are using **AWS RDS MySql**.

## Data

Our data comes from a Kaggle project (https://docs.google.com/spreadsheets/d/1lac1H2IgCDCs9LLTQL6yb6MUPN1u4C5fJv_6YjipIaM/edit#gid=1072460513) which attempted to identify important Data Science skills using keyword searches on popular social/job websites like LinkedIn, Indeed, etc. This dataset was well structured and available as a multi-sheel MS Excel download. We tidyied up in R by extracting data from multiple sheets and generating multiple CSV to populate the core data model entities (see below).  

We discussed refreshing the dataset to make it more current but the APIs required paid subscriptions and we did not have the time to explore alternatives. However, we included timestamps in all entities to make it possible for time series data to coexist within our data model.

## Data Model

We started the data model exercise by leveraging the ER modeling capabilities of MySQLWorkbench. After modeling the normalized data model entities we were able to generate the SQL scripts from schema creation from MySQLWorkbench which make it easy to forward engineer the schema on both AWS and local MySQL. The schema includes foreign key relationships and referential integrity checks and actions.  

https://github.com/himalayahall/DATA607-PROJECT3/blob/main/ER.png

Entities:

1. SOURCE  
    Souce of demand data (Linkedin, Monster, etc.)
    
3. SKILL  
    Skill and category (Software, General, Soft)
    
5. EDUCATION  
    Education level (BS, MS, etc.)
    
7. SKILL_IN_DEMAND  
    Skill demand (Source, skill, demand, etc.)
    
9. EDUCATION_IN_DEMAND  
    Education demand (Source, education, demand, etc.)

