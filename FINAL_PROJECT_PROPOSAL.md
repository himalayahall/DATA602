## Final Project Overview

This document provides an overview of the group members, tools, and data documentation for the Final Project

----------------

## Team Members

Jawaid Hakim

----------------

## Introduction

NLP (Natural Language Processing), NLU (Natural Language Understanding), and NLG (Natural Language Generation) are important subtopics of Machine 
Learning. 

**NLP** it involves programming computers to process massive volumes of language data. It involves numerous tasks that break down natural language into 
smaller elements in order to understand the relationships between those elements and how they work together. NLP focuses largely on converting text to 
structured data. It does this through the identification of named entities (a process called named entity recognition) and identification of word 
patterns, using methods like tokenization, stemming, and lemmatization, which examine the root forms of words.

**NLU** (Natural Language Understanding) is a subset of natural language processing, which uses syntactic and semantic analysis of text and speech to determine the meaning of a sentence. One of the primary goals of NLU is to teach machines how to interpret and understand language inputted by humans. 
It aims to teach computers what a body of text or spoken speech means. NLU leverages AI algorithms to recognize attributes of language such as sentiment, semantics, context, and intent. It enables computers to understand the subtleties and variations of language.

**NLG** (Natural Language Generation) is also a subset of NLP and is concerned with enabling machines to not just process and understand text but to generate text. While NLU focuses on computer reading comprehension, NLG enables computers to write. NLG is the process of producing a human language 
text response based on some data input (prompt).

## Project Goal

Recent advancements in NLP, most notable the NLG capabilities of Large Language Models (LLM) like ChatGPT, have taken the public imagination by storm. In this project we will explore the following:

- **NLP**: create a classifier to classify product reviews as either original (presumably human created and authentic) or fake (computer generated fake reviews)
-- Use [Fastai](https://docs.fast.ai) to build the classifier. This will be accomplished by taking a pretrained language model and fine-tuning it to classify reviews.  What we call a language model is a model that has been trained to guess what the next word in a text is (having read the ones before). This kind of task is called self-supervised learning: we do not need to give labels to our model, just feed it lots and lots of texts. It has a process to automatically get labels from the data, and this task isn't trivial: to properly guess the next word in a sentence, the model will have to develop an understanding of the English (or other) language.
- **NLU**: the English learned by the pretrained language model (Wikipedia) is slightly different from the English used for product reviews, so instead of jumping directly to the classifier, we will fine-tune our pretrained language model to the product corpus and then use that as the base for our classifier. This should (hopefully) result in better performance.
- **NLG**: finally, having created a language model that has been fine-tuned for product reviews, we will use it to auto-generate fake reviews. This will be done by gicing the model a starting text (prompt) and then having the model generate rest of the text (up to a maximum number of words).

## Data Sources

The generated [fake reviews dataset](https://osf.io/3vds7), containing 20k fake reviews and 20k real product reviews. OR = Original reviews (presumably human created and authentic); CG = Computer-generated fake reviews.

## Tools and Frameworks

- [Google Collab](https://colab.research.google.com)
- [Jupyter Notebook](https://jupyter.org/)
- [Fastai](https://docs.fast.ai)
