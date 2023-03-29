# Precipitation for floods in Manitoba

## API Description  
Our API offers real time precipittion for floods in Manitoba. For checking the precipitation for floods in Manitoba, you can access amount of rainfall, location and date.

## Endpoints
URI: https://weather.visualcrossing.com/VisualCrossingWebServices/rest/services/timeline/Winnipeg?unitGroup=metric&include=days&key=KPUJXVDUSAV6LY38KM4RWGEAJ&contentType=json
From VisualCrossing.com<br>

Parameters examples:
address: Winnipeg
latitude: 49.8995
longitude: -97.1411

## Resources

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
