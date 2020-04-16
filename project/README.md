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
The people who live in germany and want to explore the neighborhood or move to another neighborhood or move to a new city.


## Data
### Description of the Data:¶

#### The following data is required to answer the issues of the problem:

- List of Zipcode with corresponde geodata (latitud and longitud), population of the area.
- Venues of the city.
- Foursquare API credential.
- keyword venues from Foursquare API. You can find a list [here](https://developer.foursquare.com/docs/build-with-foursquare/categories/).

### How the data will be used to solve the problem

#### The data will be used as follows:

- Use Geojson data of Germany to locate the centroid of a zip code area.
- Use Foursquare and geopy data get desired venues
- Addresses from locations will be converted to geodata( lat, long) using Geopy-distance and Nominatim.
- Create a list with keyword venues. 
- Use Folium to plot the data.

## Methodology <a name="methodology"></a>
There is one main method **find_desired_community_germany** to find desired community in the selected city with selected keyword venues.
```python
find_desired_community_germany(city, foursquare_credential, keywordlist,limit=100, radius=500)
 
    @Param
                city, city name;
                foursquare_credential, list like, [CLIENT_ID,CLIENT_SECRET];
                keywordlist, list like, include the keyworde of interested venues, such as Supermarket, Bus Stop;
                limit, int, limit of foursquare searched venues of a point;
                radius, in meters.
    @Return
        a folium map of desired community. 
   
```
And two subfunction for the `ind_desired_community_germany`.
- `getNearbyVenues(names, latitudes, longitudes, LIMIT=100, radius=500)` to get the nearby venues.
- `find_desired_venues(keywordlist, City_venues)` to find the desired venues with keywords in the keywordlist.

## Result and Discussion <a name="results"></a>

### Case Study I
As I am study at RWTH Aachen of Germany, I would like to find my desired community in Aachen. As a Student, my selected keywords would be 'Supermarket', 'Restaurant', 'Café', 'Bus' etc.
- [Desired Community in Aachen](https://nbviewer.jupyter.org/github/RuikunLi/Capstone_Coursera/blob/master/project/results/Aachen_desired_community.html)
### Case Study II
My girlfriend and I lived in Köln an we love this city. So we would like to know if we move back to Köln in the future, where is our desired community. Our selected keywords would be 'Movie', 'Supermarket', 'Restaurant', 'Pharmacy', etc.
- [Desired Community in Köln](https://nbviewer.jupyter.org/github/RuikunLi/Capstone_Coursera/blob/master/project/results/K%C3%B6ln_desired_community.html)

### Case Study III
I lived in Duisburg for a while and a friend of mine would like to move to Duisburg. He study very hard therefore he want to find the community which may contain college facilities.The selected keywords would be 'Supermarket', 'College', 'Café', 'Zoo', etc.
- [Desired Community in Duisburg](https://nbviewer.jupyter.org/github/RuikunLi/Capstone_Coursera/blob/master/project/results/Duisburg_desired_community.html)
