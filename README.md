# Braze Take Home Assignment

1. Using this link, please create a sample JSON payload to record a new user with at least 1 custom attribute, 1 custom event, and 1 purchase. For this exercise, please provide the endpoint you used, as well as the body of the payload, there is no need for you to provide any header or API Key information.

Endpoint --> https://rest.iad-01.braze.com/users/track
becase you should "Use this [/user/track] the *POST* method on the /users/track endpoint Use this endpoint to record Custom events, Purchases, and update user profile attributes."

```json 
"attributes": [ 
 	{
 	  "external_id":"user_id",
      "string_attribute": "sherman",
      "boolean_attribute_1": true,
      "integer_attribute": 25,
      "array_attribute": ["banana", "apple"]
    }
    ],
    "events": [
    {
      "external_id": "user_id",
      "app_id" : "app_identifier",
      "name": "watched_trailer",
      "time": "2013-07-16T19:20:30+1:00"
    }  
   ],
  "purchases": [
     {
      "external_id": "user_id",
      "app_id": "app_identifier",
      "product_id": "product_name",
      "currency": "USD",
      "price": 12.12,
      "quantity": 6,
      "time": "2017-05-12T18:47:12Z",
      "properties": {
         "integer_property": 3,
         "string_property": "Russell",
         "date_property": "2014-02-02T00:00:00Z"
       } 
     }
  ],
  "partner": "partner1"
}'
```

2. Please explain the similarities and differences of collecting data with an SDK rather than an API.
  
  | *SIMILARITIES*  | *DIFFERENCES* | 
  | -------------- | ------------- |
  |                 |               |
  


3. Write a script in a programming language of your choice that uses a loop and a conditional statement to find the value of the number of dogs in the following collection of key-value pairs. Depending on what language you’re using, it is acceptable to think of this variable as either a dictionary or an array of key-value pairs. Please only use logic that is native to the language without any external libraries:
KennelCapacity = {cats: 7, hamsters: 12, birds: 21, dogs: 3, chickens: 1}
