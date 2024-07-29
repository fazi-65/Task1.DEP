# Task1.DEP
Weather Forecasting and Historical Data Application
This project is a C++ application that interacts with weather APIs to fetch and display current weather forecasts and historical weather data for specified locations. The application also supports exporting the results to CSV and JSON formats.

Features
Location Management: Add, remove, and list locations.
Weather Forecasting: Fetch and display weather forecasts from an API.
Historical Weather Data: Fetch and display historical weather data from an API.
Export Results: Export weather data to CSV and JSON formats.
Dependencies
This project uses the following libraries:

jsoncpp for JSON parsing.
libcurl for making HTTP requests.
Installation
Clone the Repository
bash
Copy code
git clone https://github.com/username/repository.git
cd repository
Install Dependencies
On Ubuntu/Debian:
bash
Copy code
sudo apt-get update
sudo apt-get install libjsoncpp-dev libcurl4-openssl-dev
On macOS (using Homebrew):
bash
Copy code
brew install jsoncpp
brew install curl
On Windows:
Download and install jsoncpp and libcurl from their respective repositories.
Follow their installation instructions.
Build the Project
To build the project, you can use g++ or CMake.

Using g++:
bash
Copy code
g++ -o weather_app main.cpp -ljsoncpp -lcurl
Using CMake:
Create a CMakeLists.txt file (see example below).
Run the following commands:
bash
Copy code
mkdir build
cd build
cmake ..
make
Example CMakeLists.txt
cmake
Copy code
cmake_minimum_required(VERSION 3.10)
project(WeatherApp)

set(CMAKE_CXX_STANDARD 17)

# Find jsoncpp and curl packages
find_package(jsoncpp REQUIRED)
find_package(CURL REQUIRED)

# Add executable
add_executable(WeatherApp main.cpp)

# Link libraries
target_link_libraries(WeatherApp jsoncpp_lib CURL::libcurl)
Usage
Edit the main.cpp file to provide your API keys and base URL for the weather API.

Run the executable:

bash
Copy code
./weather_app
The program will:

Fetch and display the current weather forecast.
Fetch and display historical weather data.
Export the results to weather_data.csv and weather_data.json.
Configuration
Update the following sections in main.cpp with your API credentials and base URL

Contact
For any questions or suggestions, please contact fmianking6565@gmail.com
