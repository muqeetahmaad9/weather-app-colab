import requests

# OpenWeather API Key (Replace with your key)
API_KEY = "your_api_key_here"
BASE_URL = "http://api.openweathermap.org/data/2.5/weather"

def get_weather(city):
    params = {"q": city, "appid": API_KEY, "units": "metric"}
    response = requests.get(BASE_URL, params=params)
    
    if response.status_code == 200:
        data = response.json()
        temp = data["main"]["temp"]
        humidity = data["main"]["humidity"]
        wind_speed = data["wind"]["speed"]
        return f"🌍 City: {city}\n🌡️ Temperature: {temp}°C\n💧 Humidity: {humidity}%\n🌬️ Wind Speed: {wind_speed} m/s"
    else:
        return "⚠️ City not found! Please enter a valid city."

# Get user input (Colab-friendly)
city = input("Enter City Name: ")
weather_info = get_weather(city)

# Display the weather information
print("\n🌦️ Weather Report:\n")
print(weather_info)
