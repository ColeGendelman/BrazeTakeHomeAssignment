# Braze Take Home Assignment

1. Using this link, please create a sample JSON payload to record a new user with at least 1 custom attribute, 1 custom event, and 1 purchase. For this exercise, please provide the endpoint you used, as well as the body of the payload, there is no need for you to provide any header or API Key information.

Assuming the new user has already been identified

Endpoint --> https://rest.iad-01.braze.com/users/track
becase you should use the **POST** method on the /users/track endpoint "to record Custom events, Purchases, and update user profile attributes."

Braze automatically creates a new user profile if the **external_id** does not exist and there is no **_update_existing_only** key with a value of **true**

```json 
{
	"attributes": [ 
 	{
 	  "external_id": "user_id",
      "first_name": "Cole",
      "age": 26
    }
    ],
    "events": [
    {
      "external_id": "user_id",
      "app_id" : "11ae5b4b-2445-4440-a04f-bf537764c9ad",
      "name": "bought_car",
      "time": "2019-11-14T13:50:10+1:00"
    }  
   ],
  "purchases": [
     {
      "external_id": "user_id",
      "app_id": "11ae5b4b-2445-4440-a04f-bf537764c9ad",
      "product_id": "Tesla",
      "currency": "USD",
      "price": 12000.00,
      "time": "2019-11-14T13:50:10+1:00",
      "properties": {
         "year": 2019,
         "model": "Y"
       } 
     }
  ]
}
```

2. Please explain the similarities and differences of collecting data with an SDK rather than an API.
  
  > SDK's usually contain one (or more) API and make it easier to call APIs in your code. 
  > An API call is used for a specific task/feature and utilizes existing functions and sources.
  > An SDK defines a function and creates a way to call the source and function.
  > For an API call you would need to include an operation
  > Both SDK's and API's have parameters you can use as well as different languages to call the endpoint.  
  


3. Write a script in a programming language of your choice that uses a loop and a conditional statement to find the value of the number of dogs in the following collection of key-value pairs. Depending on what language you’re using, it is acceptable to think of this variable as either a dictionary or an array of key-value pairs. Please only use logic that is native to the language without any external libraries:
KennelCapacity = {cats: 7, hamsters: 12, birds: 21, dogs: 3, chickens: 1}

In Python, using a dictionary
```python
for x,y in KennelCapacity.items():
  if x == "dogs":
    print (y)
```
