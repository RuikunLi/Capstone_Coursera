# Find your desired community/neighborhood in a city of Germany
## Table of contents
* [Introduction: Business Problem](#introduction)
* [Data](#data)
* [Methodology](#methodology)
* [Analysis](#analysis)
* [Results and Discussion](#results)
* [Conclusion](#conclusion)

## Introduction

When you live in Germany and want to explore your neighborhoods or you would like to move to a desired neighborhood in a city of Germany. For example, you are a non-Aachener who will work in Aachen next year and want to find your desired neighborhoods based on different venues. You can enter your priority of venues of a specific city and get the area with zip code which macths to your demand.

### target audience
The people who live in germany and want to explore the neighborhood or move to another neighborhood(postal code)

### Case Study I
As I am study at RWTH Aachen of Germany, I would like to find my desired community in Aachen. As a Student, my selected keywords would be 'Supermarket', 'Restaurant', 'Café', 'Bus' etc.

### Case Study II
My girlfriend and I lived in Köln an we love this city. So we would like to know if we move back to Köln in the future, where is our desired community. Our selected keywords would be 'Movie', 'Supermarket', 'Restaurant', 'Pharmacy', etc.


## Data
### Description of the Data:¶

#### The following data is required to answer the issues of the problem:

- List of Zipcode with corresponde geodata (latitud and longitud), population of the area.
- Venues clusters of the city.
- Venues for subway metro stations, as needed

### How the data will be used to solve the problem

#### The data will be used as follows:

- Use Geojson data of Germany to locate the centroid of a zip code area.
- Use Foursquare and geopy data to map top 10 venues and clustered in groups.
- Use foursquare and geopy data to map the location of subway metro stations , separately and on top of the above clustered map in order to be able to identify the venues and ammenities near each metro station, or explore each subway location separately
- Use Foursquare and geopy data to map the location of rental places, in some form, linked to the subway locations.
- Addresses from locations will be converted to geodata( lat, long) using Geopy-distance and Nominatim.

## Result and Discussion <a name="results"></a>

- [Desired Community in Aachen](https://nbviewer.jupyter.org/github/RuikunLi/Capstone_Coursera/blob/master/project/results/Aachen_desired_community.html)
- [Desired Community in Köln](https://nbviewer.jupyter.org/github/RuikunLi/Capstone_Coursera/blob/master/project/results/K%C3%B6ln_desired_community.html)
