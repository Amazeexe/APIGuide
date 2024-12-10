# [Important API Practices]

When Working With APIs, it is important to store your API keys in envionrment variables.
- In Python that looks as follows:
    ```
    import os
    API_KEY = os.getenv("OPENWEATHER_API_KEY")
    ```
It is also important to Respect Rate Limits 
- In Python delays can be added between requests using time.sleep():
  ```
  import time

  def fetch_data():
    for i in range(5):
        print("Fetching data...")
        time.sleep(1)  # 1-second delay
  ```
  [Previous: Weather App](06_WeatherApp.md)


   [Return to ReadMe: Understanding API Requests and Responses](README.md)
  
