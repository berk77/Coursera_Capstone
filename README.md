# The Battle of the Neighborhoods in Toronto, Canada

* This report is aimed at stakeholders who want to open a food venue in Toronto, Canada. 
* The aim is to reveal the frequency of food venues in neighborhoods. 
* Also, to offer alternative options to stakeholders by clustering similar neighborhoods.

## Data

Depending on the definition of the problem, the factors that will affect the study are as follows:
* number of existing food venues in the neighborhoods (any type of food venue)
* The most common food venues in the neighborhoods

Following data sources will be needed to extract/generate the required information:
* Information such as the postal code, borough, and neighborhood of the city of Toronto will be collected by scraping the <a href='https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M'>wikipedia</a> page.
* Toronto Neighborhood coordinates will be collected using the prepared geospatial data csv file.
* The latitude and longitude values of the city of Toronto will be collected using the geopy library.
* The number, type, location, postal code and distance of the food venues in each neighborhood will be obtained using the Foursquare API.

## Methodology

The following procedures were performed to determine the density of food venues in Toronto's neighborhoods and the type of food venues most common in the neighborhoods.

First of all, neighborhood data was taken from the wikipedia page. Afterwards, the necessary data was obtained from a csv file with neighborhood coordinates and combined. Finally, using the obtained neighborhood coordinates, food venue data were collected with the foursquare api.

After the necessary data were collected, the data preprocessing part was started. First, duplicate food venue data is extracted. Afterwards, food venues with unknown neighborhoods were assigned to the nearest neighborhood.

In the final step, a heatmap was presented to show the density of neighborhoods in terms of food venues and focused on what implications these might have for stakeholders. In addition, basic information was provided to stakeholders, taking into account the most common types of food venues in these neighborhoods. This will allow stakeholders to choose a starting point at the neighborhood level. Finally, clustering (using k-means clustering) was created to present stakeholders with different alternatives on a neighborhood basis.

## Results

The analysis shows that the busiest area in the city of Toronto in terms of food venues is the neighborhoods connected to the Downtown Toronto borough. The main ones are CN Tower, King and Spadina, Railway Lands, Harbourfront West, Bathurst Quay, South Niagara, Island airport neighborhoods. From this analysis, it can be seen that this area is a valuable area for food venues.

## Conclusion

The aim of this project was to assist stakeholders trying to find venues for a food venue in the city of Toronto. There are many factors that affect the location of a food venue. In this study, analyzes were made considering only the competition factor. First of all, all venues in the food category were collected on the basis of Neighborhoood using the Foursquare api. As a result of the analysis made afterwards, the density of food venues in the city was revealed. Thus, the competition factor at the general level was examined. Then, going a little more specific, the frequency of food venues in the neighborhoods was revealed as a result of analysis. Thus, stakeholders will be able to easily select a starting point by taking this information into consideration during the location selection phase.

#### Results are shown below
![](/images/density.png)

![](/images/cluster.png)

The notebook cannot be analyzed meaningfully because the visualizations do not appear on Github. <a href = "https://nbviewer.jupyter.org/github/berk77/Coursera_Capstone/blob/main/Capstone_Project_The_Battle_of_the_Neighborhoods_in_Toronto%2C_Canada.ipynb" >If you want, you can review the notebook here. </a>
