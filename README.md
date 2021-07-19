#Trains Project

The solution developed was a RESTful API created with ASP.NET Web API.
It has 2 projects, one for building the graph and the other to handle the API calls.
The BuildGraph in GraphBusiness.cs gets the string of the routes and distances and creates a graph with nodes and edges with its weight. It also has the AllRoutesAlgorithm.cs which contains all the logic to find the different distance and other calculations.
On the TrainsAPIController.cs you can find the procedures for each API call.
To compile and run, open the solution file 'Trains.sln' under the Trains directory and execute the WebProject TrainsAPI.
Test API with GET call on POSTMAN.
1.	The distance of the route A-B-C. 
a.	http://localhost:13672/api/TrainsAPI/RouteDistance/A-B
2.	The distance of the route A-D.
a.	http://localhost:13672/api/TrainsAPI/RouteDistance/A-D
3.	The distance of the route A-D-C. 
a.	http://localhost:13672/api/TrainsAPI/RouteDistance/A-D-C
4.	The distance of the route A-E-B-C-D. 
a.	http://localhost:13672/api/TrainsAPI/RouteDistance/A-E-B-C-D
5.	The distance of the route A-E-D.
a.	http://localhost:13672/api/TrainsAPI/RouteDistance/A-E-D
6.	The number of trips starting at C and ending at C with a maximum of 3 stops. In the test input, there are two such trips: C-D-C (2 stops), and C-E-B-C (3 stops). 
a.	http://localhost:13672/api/TrainsAPI/AvailableRoutesMaxStops/C/C/3
7.	The number of trips starting at A and ending at C with exactly 4 stops. In the test input, there are three such trips: A to C (via B,C,D); A to C (via D,C,D); and A to C (via D,E,B). 
a.	http://localhost:13672/api/TrainsAPI/AvailableRoutesNumStops/A/C/4
8.	The length of the shortest route (in terms of distance to travel) from A to C. 
a.	http://localhost:13672/api/TrainsAPI/ShortestRoute/A/C
9.	The length of the shortest route (in terms of distance to travel) from B to B. 
a.	http://localhost:13672/api/TrainsAPI/ShortestRoute/B/B
10.	The number of different routes from C to C with a distance of less than 30. In the test input, the trips are: CDC, CEBC, CEBCDC, CDCEBC, CDEBC, CEBCEBC, CEBCEBCEBC.
a.	http://localhost:13672/api/TrainsAPI/AvailableRoutesMaxDistance/C/C/30

