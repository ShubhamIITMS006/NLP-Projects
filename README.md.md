**Aspect-Based Sentiment Analysis (ABSA)**



This project implements Aspect-Based Sentiment Analysis (ABSA) using BERT and DistilBERT models. Unlike traditional sentiment analysis, which provides an overall sentiment score, ABSA identifies specific aspects of a product, service, or entity and determines the sentiment (positive, negative, neutral) towards each aspect.



**Introduction**



* ABSA provides fine-grained insights by analyzing sentiment at the aspect level (e.g., "battery life", "screen quality" in product reviews).
* This helps businesses move beyond general sentiment to understand what customers like or dislike in detail.



**Business Applications**



* E-commerce \& Retail: Analyze product reviews to improve design and highlight key strengths.
* Tech \& Electronics: Identify issues at a component level (battery, camera, display).
* Restaurants \& Hospitality: Extract sentiment for food, service, ambiance, and cleanliness.
* Customer Support \& CRM: Assess feedback on support speed, staff behavior, and resolution quality.



**Problem Statement**



The project focuses on:



* Aspect Extraction
* Sentiment Classification

for electronic devices, enabling the identification of a “Top Complaint List” from reviews.



**Dataset**



* Laptop review dataset with 6 columns.
* Preprocessing includes:

&nbsp;	Dropping unnecessary columns (from, to, id)

&nbsp;	Converting sentiment polarity to numeric form for classification

&nbsp;	Grouping reviews by sentence

&nbsp;	Applying BIO (Begin, Inside, Outside) tagging for aspect extraction



⚙️ Methodology



1. BIO Labeling



&nbsp;	B: Beginning of aspect term



&nbsp;	I: Inside aspect term



&nbsp;	O: Outside aspect term



&nbsp;	Converted to numeric classes → {O: 0, B: 1, I: 2}



2\. Model Training



&nbsp;	DistilBERT used for token classification



&nbsp;	Optimizer: Adam



&nbsp;	Loss Function: Cross Entropy Loss



3\. Implementation Details



&nbsp;	Tokenization: DistilBertTokenizerFast



&nbsp;	Model: DistilBertForTokenClassification



&nbsp;	Output: loss, logits per token

**Features**



* Aspect term extraction using BERT / DistilBERT
* Sentiment classification at aspect level
* Preprocessing pipeline with BIO tagging
* Easily extendable to other domains (hospitality, retail, support)
