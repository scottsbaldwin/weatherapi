# weatherapi

This is a repo of static files that can be used as a mock weather API for example applications.

## Date

A mock endpoint for the sever's date. The response is the Unix timestamp.

```
curl https://scottsbaldwin.github.io/weatherapi/date
```

## Locations

Gets the supported locations as an array of identifiers. Each location identifier can be used with the weather endpoint below.

```
curl https://scottsbaldwin.github.io/weatherapi/locations
```

Response:

```
[ "austin", "pune", "santabarbara" ]
```

## Weather

Gets the weather information for a supported location (from the locations endpoint above).

```
# curl https://scottsbaldwin.github.io/weatherapi/weather/<locationId>
curl https://scottsbaldwin.github.io/weatherapi/weather/austin
```

Response (excerpt):

```
{
  "lat": 30.2672,
  "lon": -97.7431,
  "timezone": "America/Chicago",
  "timezone_offset": -21600,
  "current": {
    "dt": 1638466167,
    "sunrise": 1638450665,
    "sunset": 1638487822,
    "temp": 71.22,
    "feels_like": 71.85,
    "pressure": 1020,
    "humidity": 81,
    "dew_point": 65.1,
    "uvi": 2.63,
    "clouds": 1,
    "visibility": 10000,
    "wind_speed": 1.99,
    "wind_deg": 113,
    "wind_gust": 5.01,
    "weather": [
      {
        "id": 800,
        "main": "Clear",
        "description": "clear sky",
        "icon": "01d"
      }
    ]
  },
  ...
}
```