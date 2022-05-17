# Geotagged tweets in German about air quality

This dataset consists of 2,948 georeferenced tweets in the German language, which concern the topic of air quality and have been retrieved with the Twitter Standard Streaming API. The tweets have been posted from September 6, 2021 to February 16, 2022 (near six months) and contain air-quality-related keywords in their text (the complete list of keywords can be seen in the table below). The provided geoinformation has been extracted from the tweets' text with a state-of-the-art NER implementation that is based on the XLM-RoBERTa (XLM-R) language model, while OpenStreetMap API has been used for retrieving the coordinates of each detected location.

|German keywords about air quality|
| --------- |
|Luftqualität|
|Städtische Luftverschmutzung|
|Luftschadstoff|
|schlechte Luft|
|gesunde Luft|
|Feinstaub|
|PM2,5|
|PM10|
|Feinstaubemission|
|Ozon|
|Ο3 Verschmutzung|
|Ο3 Belastung|
|Ο3 Umweltbelastung|
|O3 Schadstoff|
|Schwefeldioxid|
|SO2 Verschmutzung|
|SO2 Belastung|
|SO2 Umweltbelastung|
|SO2 Schadstoff|
|Kohlenmonoxid|
|CO Verschmutzung|
|CO Belastung|
|CO Umweltbelastung|
|CO Schadstoff|
|Stickstoffdioxid|
|NO2 Verschmutzung|
|NO2 Belastung|
|NO2 Umweltbelastung|
|NO2 Schadstoff|

## Data Organization

| Property Name | Property Type | Description |
| --------- | ----------- | ----------- |
| id | String | The unique identifier of a tweet, as provided by Twitter. |
| keyword | String | The keyword based on which a tweet was retrieved. |
| locations | Array | An array of objects that contain information about the locations that have been extracted from a tweet’s text. |
| location_fullname | String | The full location name as retrieved by the OpenStreetMap API. |
| geometry | JSON Object | A JSON object that contains information about the coordinates of the location. |
| type | String<br> (predefined value: "Point") | A field that defines the type of the coordinates. |
| coordinates | Array<br> (format \[latitude,longitude\]) | An array of Double values that refer to the latitude and longitude coordinates of the location, as retrieved by the OpenStreetMap API. |

## Licensing

This dataset is licensed under the Creative Commons Attribution-NonCommercial International Public License ([CC BY-NC](https://creativecommons.org/licenses/by-nc/4.0/)). When downloading tweets by the means of the distributed Tweet IDs, users have to be compliant with [Twitter’s Developer Agreement and Policy](https://developer.twitter.com/en/developer-terms/agreement-and-policy). By using this dataset, you agree to abide by the stipulations in the license, remain in compliance with Twitter’s Terms of Service, and cite the following manuscript.

## How to Cite

S. Andreadis, M. Elias, T. Mavropoulos, C. Papadopoulos, N. Pantelidis, I. Gialampoukidis, and I. Kompatsiaris, "SPARQL querying for validating the usage of automatically georeferenced social media data as human sensors for air quality", 2022 IEEE 14th Image, Video, and Multidimensional Signal  Processing Workshop (IVMSP 2022), 26-29 June 2022, Nafplio, Greece (accepted for publication).

BibTeX:

    TBA

## Contact

If you have any further questions about the dataset or if you are interested in running some additional analyses on the data, please contact Stelios Andreadis at **[andreadisst@iti.gr](mailto:andreadisst@iti.gr)**.

## Team

Stelios Andreadis, Nick Pantelidis, Charis Papadopoulos, Thanassis Mavropoulos, Ilias Gialampoukidis, Stefanos Vrochidis, Ioannis Kompatsiaris

Information Technologies Institute (ITI), Centre for Research and Technology Hellas (CERTH)

