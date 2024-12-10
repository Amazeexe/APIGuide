# Building A simple Weather App within Python.
This App was done in Python but the principles remain the same for other coding enviornments.
## Code:
```
def fetch_weather(city):
    API_KEY = "your_api_key_here"
    BASE_URL = "http://api.openweathermap.org/data/2.5/weather"
    params = {"q": city, "appid": API_KEY, "units": "metric"}
    
    response = requests.get(BASE_URL, params=params)
    if response.status_code == 200:
        data = response.json()
        return {
            "city": data["name"],
            "temperature": data["main"]["temp"],
            "description": data["weather"][0]["description"]
        }
    else:
        return {"error": "City not found or API error."}

city_name = input("Enter city name: ")
result = fetch_weather(city_name)

if "error" in result:
    print(result["error"])
else:
    print(f"Weather in {result['city']}: {result['description'].capitalize()}")
    print(f"Temperature: {result['temperature']}°C")

```
[Previous: Understanding API Requests and Responses](05_Python_Code.md)

[Next: Understanding API Requests and Responses](07_Important_pracices)
