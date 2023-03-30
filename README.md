# Precipitation for floods in Manitoba

## API Description  
Our API offers real time precipitition data and how its amount can reflect floods in Manitoba. For checking the precipitation that cause floods in Manitoba, you can access amount of rainfall, location and date.

## Endpoints and parameters
URI: https://weather.visualcrossing.com/VisualCrossingWebServices/rest/services/timeline/Winnipeg?unitGroup=metric&include=days&key=KPUJXVDUSAV6LY38KM4RWGEAJ&contentType=json
From VisualCrossing.com<br>

_Note: Endpoints are focused mainly on the GET methods._

**Parameters examples:**  

location: ```e.g. Winnipeg``` 

__date (dd/mm/yyyy):__ ```e.g. 30/03/2023```  

amount of rainfall (mm): ```e.g. 20```

__latitude:__ ```e.g 49.8995```  

__longitude:__ ```e.g -97.1411```


## Resources

_Aside: Sources with reliable precipitation/ flooding data for Manitoba, Canada: https://www.gov.mb.ca/mit/floodinfo/index.html_ 


Placement for paragraph

```
{ 
    "type": "resources",
    "id": "1",
    "attributes": {
        "title": "Precipitation Manitoba"
    },
    "relationships": {
        "author": {
            "links": {
                "self": "https://precipitationmanitoba.ca/floods"
            }
            "data": {"type": "weather", "id": "1"}
        }
    }
} 
```

### Sample request:

curl -X 'GET' \ <br>
https://weather.visualcrossing.com/VisualCrossingWebServices/rest/services/timeline/Winnipeg?unitGroup=metric&include=days&key=KPUJXVDUSAV6LY38KM4RWGEAJ&contentType=json<br>
 -H 'accept: application/json'<br>
 
 Precipitation:  
 ```https://weather.visualcrossing.com?location=AssiniboineRiver,rainfall=56&date=1978-08-17``

 
### Sample response: 
 
You will find the result from the endpoint GET: ___ formatted in JSON below. 

```
{
   "results":
   {
       "river_name": "Assiniboine River",
       "flood_likelihood": 75

       
   }
}
```
