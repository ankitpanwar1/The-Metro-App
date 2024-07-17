# The-Metro-App
This project is a Metro Transit System simulator. It allows users to interact with a digital representation of the metro system, find routes, and get information about stations and travel times.
Key Components:

Graph Class:
This is the core of the system, representing the metro network.
Vertex Class:
Represents individual stations in the network.
Main Program:
Handles user interaction and calls appropriate functions.

Metro Lines:
The system models five metro lines, each represented by an enum:

Purple
Green
Yellow
Pink
Blue

Key Functions and Their Purposes:

createStations():

Initializes all stations in the network.
Adds each station to the graph with its name, line color, and station code.


createLinks():

Establishes connections between stations.
Adds edges between adjacent stations with their distances.


addVertex(string vname, Line code, int st_code):

Adds a new station to the network.


addEdge(string v_name1, string v_name2, int val):

Connects two stations with a given distance.


displayMap():

Prints the entire metro map, showing connections between stations.


displayStation():

Lists all stations with their names, lines, and codes.


dijkstra_shortest_dist():

Finds the shortest path between two stations based on the number of stops.


dijkstra_shortest_time():

Finds the fastest route between two stations based on travel time.


countInterchanges():

Calculates the number of line changes in a given route.


setPath():

Constructs a human-readable string describing the route.


tranformToUpper() and tranformToLower():

Utility functions for string case conversion.



Main Program Flow:

The program starts by creating a Graph object, which initializes the entire metro network.
It then enters a loop, presenting the user with a menu of options:

List all stations
Find minimum cost between two stations
Find shortest time between two stations
Get minimum cost path between two stations
Get shortest time path between two stations
Exit


Based on the user's choice, it calls the appropriate functions:

For listing stations, it calls displayStation().
For finding routes, it asks for source and destination stations, then calls the appropriate Dijkstra algorithm function.


The results are then displayed to the user, showing:

Total distance or time
Number of stops
Number of interchanges
The full path (if requested)


This process repeats until the user chooses to exit.

Additional Features:

The system handles input in various forms (station names, serial numbers, or codes).
It uses case-insensitive string matching for station names.
The project implements error handling for invalid inputs.

In summary, this project simulates a complex metro system, allowing users to navigate it efficiently by finding optimal routes based on different criteria (distance or time). It demonstrates the application of graph theory and pathfinding algorithms in a real-world scenario.
