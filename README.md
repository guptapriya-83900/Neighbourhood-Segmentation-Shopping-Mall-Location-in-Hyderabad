# Neighbourhood-Segmentation-Using-Foursquare
The objective of this capstone project is to analyze and select the best locations in the city of Hyderabad, India to open a new shopping mall. Using data science methodology and machine learning techniques like clustering, this project aims to provide solutions to answer the business question.

## Data
To solve the problem, we will need the following data:

• List of neighbourhoods in Hyderabad. This defines the scope of this project which is confined to the city of Hyderabad, the capital city of Telangana which is in South India

• Latitude and longitude coordinates of those neighbourhoods. This is required in order to plot the map and also to get the venue data

• Venue data, particularly data related to shopping malls. We will use this data to perform clustering on the neighbourhoods

This Wikipedia page https://en.wikipedia.org/wiki/Category:Neighbourhoods_in_Hyderabad,_India is a list of neighbourhoods in Hyderabad, with a total of 200 neighbourhoods. We will use web scraping techniques to extract the data from the Wikipedia page, with the help of Python requests and beautifulsoup packages. Then we will get the geographical coordinates of the neighbourhoods using Python Geocoder package which will give us the latitude and longitude coordinates of the neighbourhoods. After that, we will use Foursquare API to get the venue data for those neighbourhoods. Foursquare API will provide many categories of the venue data, we are particularly interested in the Shopping Mall category in order to help us to solve the business problem put forward. This is a project that will make use of many data science skills, from web scraping (Wikipedia), working with API (Foursquare), data cleaning, data wrangling, to machine learning (K-means clustering) and map visualization (Folium).


## Model
After gathering the data, we will populate the data into a pandas DataFrame and then visualize the neighbourhoods in a map using Folium package. This allows us to perform a sanity check to make sure that the geographical coordinates data returned by Geocoder are correctly plotted in the city of Hyderabad. With the data, we can check how many venues were returned for each neighbourhood and examine how many unique categories can be curated from all the returned venues and then we will analyse each neighbourhood.We will cluster the neighbourhoods into 3 clusters based on their frequency of occurrence for “Shopping Mall”. The results will allow us to identify which neighbourhoods have a higher concentration of shopping malls while which neighbourhoods have a fewer number of shopping malls. Based on the occurrence of shopping malls in different neighbourhoods, it will help us to answer the question as to which neighbourhoods are most suitable to open new shopping malls. Therefore, this project recommends property developers to capitalize on these findings to open new shopping malls in neighbourhoods in cluster 0 with little to no competition.


## Results
The results from the k-means clustering show that we can categorize the neighbourhoods into 3 clusters based on the frequency of occurrence for “Shopping Mall”:

• Cluster 0: Neighbourhoods with no shopping malls

• Cluster 1: Neighbourhoods with a moderate concentration of shopping malls

• Cluster 2: Neighbourhoods with a very high concentration of shopping malls

The results of the clustering are visualized in the map with cluster 0 in red colour, cluster 1 in purple colour, and cluster 2 in mint green colour.
