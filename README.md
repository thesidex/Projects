# Trains

##Problem Description

You have been tasked to help the Kiwiland railroad provide information about its routes to its customers, in particular:
route distance, number of unique routes between two towns, and the shortest route between two towns. In Kiwiland,
all train routes are one-way, and round trip routes may or may not exist. For example, just because there is a route
from town A to B does not mean there is necessarily a route from B to A. In fact, if both routes happen to exist, each
route should be considered unique (and may even have different distances)!
Use a directed graph to represent the train routes. A node represents a town and an edge represents a route between
two towns. The edge weight represents route distance. No route appears more than once in the input, and for any
given route, the starting and ending town will never be the same town (e.g., there are no routes from A to A).
Given the test inputs, calculate the following:
1. The distance of the route A-B-C.
2. The distance of the route A-D.
3. The distance of the route A-D-C.
4. The distance of the route A-E-B-C-D.
5. The distance of the route A-E-D.
6. The number of trips starting at C and ending at C with a maximum of 3
stops. In the test input, there are two such trips: C-D-C (2 stops). and C-E-B-C
(3 stops).
7. The number of trips starting at A and ending at C with exactly 4 stops. In the
test input, there are three such trips: A to C (via B,C,D); A to C (via D,C,D); and
A to C (via D,E,B).
8. The length of the shortest route (in terms of distance to travel) from A to C.
9. The length of the shortest route (in terms of distance to travel) from B to B.
10. The number of different routes from C to C with a distance of less than 30. In
the test input, the trips are: CDC, CEBC, CEBCDC, CDCEBC, CDEBC, CEBCEBC,
CEBCEBCEBC.
For items 1 through 5, if no such route exists, output ‘NO SUCH ROUTE’.
Otherwise, follow the route as given; do not make any extra stops!


##Solution
		Trains Project

The solution developed was a RESTful API created with ASP.NET Web API.
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

