# Wind Widget

A real-time wind visualization widget styled after iOS widgets. Displays current wind speed and direction with animated particle effects that respond to wind intensity.

## Demo

View the live demo: https://jwzy.github.io/wind-widget/

## Features

- **Real-time wind data** - Fetches current wind speed and direction for your location
- **Animated particles** - Wind streaks that adjust speed, density, and opacity based on wind intensity
- **Location detection** - Automatically detects your location and displays the city name
- **Manual controls** - Override wind speed and direction with the control panel
- **Auto-refresh** - Updates live data every 5 minutes

## APIs Used

| API | Purpose |
|-----|---------|
| [Browser Geolocation API](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API) | Detects user's coordinates |
| [BigDataCloud Reverse Geocoding](https://www.bigdatacloud.com/free-api/free-reverse-geocode-to-city-api) | Converts coordinates to city name |
| [Open-Meteo](https://open-meteo.com/) | Fetches current wind speed and direction |

## How It Works

1. On load, requests location permission from the browser
2. If granted, fetches coordinates and reverse geocodes to get the city name
3. Queries Open-Meteo for current wind conditions at those coordinates
4. Renders an iOS-style widget with animated wind particles
5. Falls back to Tokyo if location access is denied
