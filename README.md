# Pricing Strategy Airbnb based on Negative Reviews

Do higher prices of Airbnb accommodations result in a higher relative number of negative reviews for the specific accommodation?


## Motivation

The success of online marketplaces depends not only on how easily buyers can find the right sellers for them, but also on the level of trust there is prevalent. Feedback systems can help in establishing this trust ([Tadelis, 2016](https://www.annualreviews.org/doi/abs/10.1146/annurev-economics-080315-015325)). For the design of feedback systems, it is important to understand how reviews are generated and whether these can be influenced by agents ([Carnehl et al., 2021](http://www.kevintran.eu/files/airbnb_ratings_paper.pdf)).

This research will focus on how prices may influence the relative amount of negative reviews for Airbnb accommodations. [Carnehl et al. (2021)](http://www.kevintran.eu/files/airbnb_ratings_paper.pdf) explains three consecutive consequences for pricing and reviews:
- High prices lead to high expectations
- High expectations lead to more chances for dissatisfaction
- Dissatisfaction leads to more negative reviews

Concretely, this study investigates the relationship between price and negative reviews. In this way, it can be studied whether:
- Charging a higher price is a risk in terms of setting the expectations too high, resulting in more negative reviews or;
- Charging a higher price does not lead to more negative reviews, as expectations are likely to be met. 
Eventually, there is also a possibility that there is no significant correlation between these two variables. 

With the results of this analysis, Airbnb hosts can decide upon which price to charge for their accommodation with the results of this study in mind. Carefully setting the price of an accommodation can prevent dissatisfied customers and possible accompanying negative consequences.

## Data

For this project, available Airbnb data is used from [Inside Airbnb](http://insideairbnb.com/get-the-data.html). Both datasets which were used are about Airbnb listings and reviews in Amsterdam, North Holland, The Netherlands. 

<img src="https://60days.nl/wp-content/uploads/2016/12/airbnb-amsterdam.jpg" width="450">

## Method and results

The method used to indicate the amount of negative reviews per accommodation is a sentiment analysis. Sentiment analysis is used to identify how sentiments are used in text and if they indicate a positive or negative opinion toward the subject ([Nasukawa, 2003](https://dl.acm.org/doi/pdf/10.1145/945645.945658)). We will use this to classify whether a review is positive, negative or neutral. 

To expand the sentiment analysis, we will also make use of a text analysis. By using a text analysis we will identify 10 topics amongst all reviews generated. With this we can see what topic is defined in the review and then see whether there are positive, negative or neutral reviews associated with this topic.

(First, introduce and motivate your chosen method, and explain how it contributes to solving the research question/business problem.

Second, summarize your results concisely. Make use of subheaders where appropriate.)

## Repository overview

This repository consists of three folders (code, docs, and gen/output), and three files (.gitignore, README.md, and dprep21.Rproj). The motivation, instruction and results of this project are to be found in the README.md file, which is the currently displayed file. The data for this project is stored in a cloud service, which can be downloaded using the download_data.r script provided in the code. When running the code a new folder 'data' will be generated where the raw data will be stored.

In the code folder a makefile is included which will enable the user to automatically run the code included for this project in order to build the project and view the results.

## Running instructions

### Required software

- Install [Make](https://tilburgsciencehub.com/building-blocks/configure-your-computer/automation-and-workflows/make/). Make is required in order to run the automated pipeline.   Using this 'build tool' enables easier reproduction of the workflow and allows for more transparancy in the project
- Install [R and RStudio](https://tilburgsciencehub.com/building-blocks/configure-your-computer/statistics-and-computation/r/).
- In R, the following packages should be installed by copy/pasting and running the following code snippet:
```
install.packages("googledrive")
install.packages("readr")
install.packages("tidyverse")
install.packages("dplyr")
install.packages("lubridate")
install.packages("gtsummary")
install.packages("textstem")
install.packages("vader")
install.packages("yardstick")
install.packages("stm")
install.packages("ggplot2")
install.packages("ggraph")
```
- Required data will be downloaded from a Google Drive document. Thus, you should have a Google Drive account to access the data files.

### Collecting the data

The data required for this project is available on [Inside Airbnb](http://insideairbnb.com/get-the-data.html), the datasets used in this project are [listings.csv](http://data.insideairbnb.com/the-netherlands/north-holland/amsterdam/2021-09-07/visualisations/listings.csv) and [Inside Airbnb](http://data.insideairbnb.com/the-netherlands/north-holland/amsterdam/2021-09-07/visualisations/reviews.csv). There is a script included which allows access to the Google Drive where the exact set used in this project is stored.

### Running the workflow

## More resources

- Additional information about the Airbnb locations in [Amsterdam](http://insideairbnb.com/amsterdam/).
- Research on [reviews and price on online platforms in Boston](https://scholar.google.com/scholar?output=instlink&q=info:ZXRx9yxPYn8J:scholar.google.com/&hl=en&as_sdt=0,5&scillfp=10945875589668552579&oi=lle). 

## About

This study is conducted for the [Data Preparation and Workflow Management](https://dprep.hannesdatta.com/) course of the TISEM department of Tilburg University. This course is part of the master Marketing Analytics program. The study is conducted by team 4 with the following members: [Noa Beekmans](https://github.com/noa-beekmans), [Pien Korteweg](https://github.com/eakorteweg), [Rashel Mol](https://github.com/Rashel-Mol), [Astrid Raaijmakers](https://github.com/AstridR97), [Amber Vermeer](https://github.com/AmberVermeer). Professor [Hannes Datta](https://github.com/hannesdatta) supervised the study and provided feedback.
