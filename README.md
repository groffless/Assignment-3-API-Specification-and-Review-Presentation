# Precipitation Manitoba

## API Description  
Our API offers real time precipitation data and how its amount can reflect floods in Manitoba. For checking the precipitation that causes floods in Manitoba, you can access the amount of precipitation through inputs of the location and date. 

## Endpoints and Parameters
There is one request you can make which includes a GET of the precipitation from the required field's date, latitude and longitude (of location in Manitoba).


### Parameters:
All the parameters for the GET request is ___required___.

- __date:__  Date formatted as (string) dd/mm/yyyy
    - ```e.g. 30/03/2023```  

- __latitude:__ Latitude as decimal (number/float)
    - ```e.g 49.8995```  

- __longitude:__ Longitude as decimal (number/float)
    - ```e.g -97.1411```


## Resources

```
{ 
    "type": "resources",
    "id": "1",
    "attributes": {
        "title": "precipitation"
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

Submit a request through the curl command with the 3 required parameters (date, latitude and longitude).

curl -X 'GET' \
  'https://precipitation.mb.swagger.io/api/v1/precipitation?longitude=-97.1411&latitude=49.8995&date=01%2F04%2F2023' \
  -H 'accept: application/json'

### Sample response: 
 
You will find the result from the endpoint GET: precipitation formatted in JSON below. 

```
{
   "results":
   {
       "river_name": "Assiniboine River",
       "flood_likelihood": 75
       "rainfall": 22
   }
}
```
