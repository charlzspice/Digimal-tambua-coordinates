# Digimal-tambua-coordinates
an algorithm to do geocoding  of Kenya administrative units to get the coordinates of Villages in Kenya
## Geocoding Algorithm Explanation

###Introduction
Geocoding is the process of converting addresses (like "1600 Amphitheatre Parkway, Mountain View, CA") into geographic coordinates (like latitude 37.423021 and longitude -122.083739), which you can use to place markers on a map, or position the map.

### Overview
The geocoding algorithm implemented in this HTML document utilizes the MapQuest Geocoding API to convert village names into latitude and longitude coordinates. Here's a breakdown of how it works:

1. **User Input**: The user selects a village from a series of dropdown menus representing the hierarchical structure of administrative regions in Kenya (county, sub-county, ward, location, sub-location, village).

2. **Data Retrieval**: When the user selects a village, the algorithm extracts the name of the village from the dropdown menu.

3. **API Request Construction**: The village name is combined with "Kenya" to form an address string. This string is then used to construct a request URL for the MapQuest Geocoding API.

4. **API Request**: The constructed URL is used to make a GET request to the MapQuest Geocoding API. This request includes the address string and an API key for authentication.

5. **Response Processing**: The API responds with geolocation data in JSON format. The algorithm parses this data to extract the latitude and longitude coordinates of the village.

6. **Coordinate Validation**: Before displaying the marker on the map, the algorithm checks if the retrieved latitude and longitude fall within the bounds of Kenya. This helps ensure that only valid coordinates are used.

7. **Marker Display**: If the coordinates are valid, a marker is placed on the Leaflet map at the location corresponding to the village. Additionally, a popup is attached to the marker displaying the name of the village.

8. **Data Storage**: The algorithm also stores the retrieved coordinates along with the village name in an array.

9. **Data Export**: Finally, the array containing the village names and coordinates is converted to JSON format. This JSON data is then prepared for download by creating a temporary URL, a link element, and triggering a simulated click event to initiate the download.

