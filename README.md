# Capstone Project Report

Week 04 Assignment

### 1. Introduction

#### a) Description of the problem:

* Running a café or restaurant is not easy. The business owners have to invest a lot of money and time to train their staff as well as buying equipment etc. But no matter how much money invested, choosing a wrong place to start the business ruins everything.

* Hospitality businesses rely on the area where there are demands and competition so much. Where will be the places that suitable to run the business?

* This capstone project collects available data of existing restaurants around Melbourne’s inner suburbs then uses a machine learning algorithm to cluster the areas.

* The clusters provide an idea of the potential areas to start running a restaurant in Melbourne in a way that will be neither too specific nor general. 

#### b) Background discussion:

* The chosen city is Melbourne as the author is living here. Melbourne is one of the biggest cities in Australia. And it is famous for the hospitality culture. It is very easy to find a restaurant in Melbourne even you are in its surrounding suburbs. Melbourne people love to dine out. Sounds it is easy to make money by running a restaurant in Melbourne, isn’t it? It may not.

* Imagine we run a restaurant with well-trained staff and delicious menu at reasonable prices, but we wanted to save the rent, so we do our business in the area that provides us cheap rental cost (of course, this area is not bustling). We ended up having no customers but still have to pay the bills.

* Or imagine we run a restaurant in a crowded area with so many competitors around us. The rental cost, in this case, is inevitable high. We have to pay for all the expensive costs. Does the chance of getting customers from the same pool as our competitors worth?

### 2. Data description

* Multiple numpy arrays to hold the lists of Melbourne’s inner suburbs. This information will be used by Foursquare API to generate a dataframe that holds the suburb’s geographical data including postal code, latitude and longitude.

* The generated suburb’s geographical data dataframe will then be used by Foursquare API again to generate a dataframe of all venues found that holds information such as venue’s suburb, venue’s category, venue’s location, venue’s geographical data etc.

* When the dataframe of all venues is generating, extra information will be added including ‘chance of getting customers’ and ‘competition rate’ (author’s subjective information based on his real-life knowledge of the areas). This information will be used later by the machine learning algorithm to cluster the areas.

* With generated necessary dataframes, it is possible to apply K-means clustering algorithm with a user’s chosen number of clusters (maximum: 12). After running the algorithm, each row in the venues dataframe will be assigned a new label. Each label represents for different clusters.

* All processed data will be together used for generating a map of clustered areas. Different colors for different clusters, information such as ‘chance of getting customers’ and ‘competition rate’ of each cluster will also be displayed.
