# SoftwareEngineeringHelp


## Appending a list
This Python script is designed to track the cities a user has visited from a predefined list.

The script starts by defining a list of cities in Australia. The print(cities) statement is used to display this list to the user.

Next, an empty list visited_cities is created. This list will be used to store the names of cities that the user has visited.

The script then prompts the user to enter the name of a city they have visited using the input() function. The entered city is stored in the variable destination.

A while loop is then initiated. This loop will continue to execute as long as the user enters a city name (i.e., as long as destination is not an empty string).

Inside the while loop, the script checks if the entered city is in the predefined list of cities using the in keyword. If the city is in the list, it is appended to the visited_cities list using the append() method. If the city is not in the list, the script prints "Invalid city" to let the user know they have entered an invalid city name.

After each iteration of the while loop, the user is prompted to enter another city. This continues until the user enters an empty string, at which point the while loop terminates.

Finally, the script prints "You have visited the following cities: " and then iterates over the visited_cities list, printing each city on a new line. This provides the user with a summary of the cities they have visited.



## Jasmine G

### Working with a list to keep track of past searches. Organising code into blocks. Load your data before you try to run/interact with the user. Make 'to be completed' modules using 'pass' as place holders.

The script begins by importing necessary libraries: os, requests, and json. The os library is used to clear the console screen, requests is used to make HTTP requests to the OpenWeatherMap API, and json is used to parse the JSON response from the API.

A global list past_searches is defined to keep track of the user's past search locations. An API key for OpenWeatherMap is also defined.

The clear function is defined to clear the console screen. It checks if the operating system is Windows (denoted by 'nt') and if so, it executes the 'cls' command to clear the console.

The start function is defined to print a welcome message and a menu of options to the user. The options include searching by location, viewing the last search, and getting help.

The get_weather function takes a location as input and makes GET requests to the OpenWeatherMap API to fetch the current weather and 5-day forecast for that location. It parses the JSON responses and extracts the necessary data, such as temperature and weather description. It then returns the current temperature, current weather, and forecast.

The search_location function prompts the user to enter a location, calls the get_weather function to get the weather data for that location, and prints the current weather conditions. It also adds the location to the past_searches list.

The view_past_searches function prints the locations in the past_searches list.

The help function is currently empty and does nothing.

The main loop of the script clears the console, prints the start menu, and then continuously prompts the user to enter a menu option. Depending on the user's input, it calls the appropriate function. If the user enters an invalid option, it prints an error message and breaks the loop