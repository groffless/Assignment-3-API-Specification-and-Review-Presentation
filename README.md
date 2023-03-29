# Precipitation for floods in Manitoba

## API Description  
Our API offers real time precipittion data and how its amount can reflect floods in Manitoba. For checking the precipitation that cause floods in Manitoba, you can access amount of rainfall, location and date.

## Endpoints with parameters
URI: https://weather.visualcrossing.com/VisualCrossingWebServices/rest/services/timeline/Winnipeg?unitGroup=metric&include=days&key=KPUJXVDUSAV6LY38KM4RWGEAJ&contentType=json
From VisualCrossing.com<br>

**Parameters examples:**  

address/location: Winnipeg  

date: dd/mm/yyy  

amount of rainfall: (mm)

latitude: 49.8995  

longitude: -97.1411  


## Resources

_Sources with reliable precipitation/ flooding data for Manitoba, Canada: https://www.gov.mb.ca/mit/floodinfo/index.html_ 


Placement for paragraph

```
{ 
    "type": "resources",
    "id": "",
    "attributes": {
        "title": ""
    },
    "relationships": {
        "author": {
            "links": {
                "self": "https://website"
            }
            "data": {"type": "weather", "id": ""}
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
    "data":
    {
        "warning": "Small amount of flooding in ___"
        
    }
}
```
2.Precipitation:
```

{
   "results":
   {
       "river_name": "Assiniboine River",
       "flood_likelihood": 75

       
   }
}
```
