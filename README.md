# Weather App

A simple and user-friendly weather application that allows users to check the current weather based on their location or search for any city's weather. The app provides the option to switch between temperature units (Celsius and Fahrenheit), and stores the user's preference for future sessions.

## Features

- **Current Weather Information**: Get up-to-date weather information for your current location or any city you search for.
- **Temperature Units**: Switch between Celsius and Fahrenheit for temperature display.
- **Persistent Settings**: The app remembers your preferred temperature unit across sessions (Celsius or Fahrenheit).
- **User-Friendly UI**: Simple and intuitive interface for a smooth user experience.

## Technologies Used

- **Kotlin**: The app is developed using Kotlin, a modern programming language for Android development.
- **Retrofit + OkHttp**: Handles API requests efficiently, with OkHttp for network management and caching.
- **Gson**: Used as the JSON converter to parse weather data from the API.
- **BlurView**: Enhances the UI with smooth and aesthetically pleasing blur effects.
- **Glide**: Optimizes image loading and improves scrolling performance.
- **Android Jetpack Components**: Includes ViewModel, LiveData for efficient state management and data persistence.
## How to Use

### 1. Get Weather Information:
- Upon opening the app, it will show the current weather of your location (if location permission is granted).
- You can also search for any city by typing the city's name in the search bar.

### 2. Change Temperature Units:
- Use the toggle switch in the settings to switch between Celsius and Fahrenheit.
- The app will remember your selection and retain it even when you come back to the settings later.

### 3. Settings:
- In the settings screen, you can change the temperature unit (Celsius or Fahrenheit). The switch will reflect your current preference.

## Code Structure
The app follows the MVVM (Model-View-ViewModel) architecture for better maintainability and scalability.
 com.example.firstapp/
│── activity/                     # UI Layer (Activities)
│   ├── AddCityActivity.kt           # Activity for adding a city
│   ├── isNetworkAvailable.kt        # Utility function to check network availability
│   ├── MainActivity.kt              # Main screen displaying weather details
│   ├── SettingActivity.kt           # Settings screen for changing temperature units
│
│── adapter/                      # RecyclerView Adapters
│   ├── CityAdapter.kt               # Adapter for displaying a list of cities
│   ├── ForecastAdapter.kt           # Adapter for displaying weather forecasts
│
│── model/                        # Data Models (Kotlin data classes)
│   ├── CityResponseApi.kt           # Data model for city information
│   ├── CurrentResponseApi.kt        # Data model for current weather data
│   ├── ForecastResponseApi.kt       # Data model for weather forecast data
│
│── repository/                   # Repository Layer (Handles API calls and data storage)
│   ├── CityRepository.kt            # Manages city-related data and API interactions
│   ├── WeatherRepository.kt         # Manages weather data fetching and caching
│
│── server/                       # API Handling (Retrofit + OkHttp)
│   ├── ApiClient.kt                 # Retrofit instance with OkHttp client
│   ├── ApiServices.kt               # API interface defining network requests
│
│── shared/                       # Shared Preferences & Utility Classes
│   ├── SharedData.kt                # Handles user preferences (temperature unit, selected city)
│
│── viewmodel/                    # ViewModels (Business logic & UI communication)
│   ├── CityViewModel.kt             # Handles city selection and management logic
│   ├── UnitViewModel.kt             # Manages temperature unit settings
│   ├── WeatherViewModel.kt          # Handles fetching and updating weather data
│
│── AndroidManifest.xml           # Android Manifest file
│── build.gradle                  # Gradle dependencies and project configuration


## Future Enhancements

- **Hourly Forecast**: Add an hourly forecast feature to display the weather for the upcoming hours.
- **Weather Maps**: Integrate weather maps to show precipitation, temperature, and cloud coverage.
- **Push Notifications**: Notify users about severe weather conditions or daily weather summaries.
