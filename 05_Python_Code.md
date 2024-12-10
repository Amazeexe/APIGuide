### [Example Implementation in Python](05_Python_Code.md)
1. Enter your API key "your_api_key_here
2. Enter the selected city into the "city" variable.


**Python Example:**  
```python
import requests

API_KEY = "your_api_key_here"
city = "London"
response = requests.get(f"http://api.openweathermap.org/data/2.5/weather?q={city}&appid={API_KEY}&units=metric")

if response.status_code == 200:
    data = response.json()
    print(f"Temperature in {city}: {data['main']['temp']}°C")
else:
    print("Error: Unable to fetch data")
```

[Previous: Public API](04_Public_API.md)

[Next: Weather App](06_WeatherApp.md)
