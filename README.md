# Road Trip Itinerary Builder

A small Python project that uses two SheCodes APIs to build a simple road trip planner.  
The script asks for a start city, a destination, and the number of days you plan to stay.  
It then calls the SheCodes Weather API and the SheCodes AI API to generate a lightweight itinerary with weather and budget friendly suggestions.

## Features

* Asks the user for a start city, destination, and trip length in days  
* Uses the SheCodes AI API to describe the driving distance between the two cities  
* Uses the SheCodes Weather API to show current weather in both the start city and the destination  
* For each day of the trip, calls the AI API to create
  * one place to eat with an estimated cost in \$00.00 format  
  * one place to visit or explore with an estimated cost in \$00.00 format  
* Prints the full plan in a simple text format that works in a terminal or Colab

## Tech stack

* Python  
* Requests  
* Jupyter or Google Colab (optional but convenient)

## APIs used

* SheCodes Weather API  
* SheCodes AI API  

You need your own SheCodes API key to run the project.

## How it works

1. The script prompts the user for
   * start city  
   * destination  
   * number of days at the destination  

2. It sends a request to the SheCodes AI API with a natural language prompt to estimate the driving distance between the two cities.

3. It sends requests to the SheCodes Weather API to fetch current weather for the start city and the destination.

4. For each day of the trip it calls the AI API again with a structured prompt that asks for:
   * exactly two bullet points with emojis  
   * one restaurant suggestion with a price  
   * one activity or place to visit with a price  

5. The script prints a daily summary that includes the date, the expected weather, and the two itinerary items.

## Getting started

### Run in Google Colab

1. Open the notebook file `road_trip_itinerary_builder.ipynb` in Google Colab.  
2. Run the first cell and enter your SheCodes API key when prompted.  
3. Run the rest of the cells and follow the text prompts in the notebook.
