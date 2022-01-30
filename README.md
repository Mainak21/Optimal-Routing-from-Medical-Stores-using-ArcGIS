# Optimal-routing-from-medical-stores-using-ArcGIS

This is the course project of GNR 615 - Geographic Information Systems (GIS) Lab course of CSRE, IIT Bombay.

The project has been done in premium ArcGIS Python API in ArcGIS online notebook.

## Introduction

Optimal routing is the process of finding most cost-effective route for multiple stops. In this project, we have estimated the optimized routes from a set of medical stores to different delivery addresses for specific medicines. For that, we have used ArcGIS Python API in ArcGIS online notebook of CSRE IITB authorized user ids. ArcGIS Python API is one of the best platforms to do different types of customized network analysis based on the requirements. The solve_vehicle_routing_problem tool has been used from ArcGIS network analysis module. In the result, the optimized routes of those stores have been shown which have the required medicine individually in map view.

## Motivation 

Optimal routing is not just to find the fastest time to reach or shortest distance between two points, but it’s the process to minimize drive time for multiple stops. Hence, it’s very much critical for the delivery business. Humans can’t find out these routes manually within a short span of time, so we need algorithms and that encourages us to root out and apply these algorithms in real life delivery problems. We have found out the most optimized routes to deliver the needed medicines to different addresses from multiple stores. Route optimizations has significant roles in business point of view, as well as natural resources too. Like,
- It reduces the driving time, so that vehicles can go to multiple stops within a short time.
- As it decreases driving time for specific stops, fuels are used less and fuel costs are reduced, which is better for natural resources too.
- It diminishes operational costs and mounts up the profits for business.
- For cab companies, drivers are able to improve customer satisfaction by usingoptimized routes.

## Methodology

- The data consists of medical stores (stores.csv), customers (customers.csv), routes of each stores (testroutes.csv).
- All the files are imported in the ArcGIS Notebook using Python API.
- Stores data has spatial information of longitude and latitude, and we use to geocode the dataset into the map.
- Customers data is imported to the map by using geocoded addresses. Then we open the ArcGIS map in Mumbai area and got all the data inputs.
- Then the routes dataset (testroutes.csv) of all the medical stores are imported, but we need only those routes which stores have Metformin medicines.
- Sothe stores dataset are sorted out, where the Metformin medicines are available and then create the dataset as “stores_med.csv”.
- Then the new routes dataset has been created as “routes_med.csv” according to the ‘stores_med.csv’ data set and then created the json file “routes_med.json” in online from the new routes dataset.
- After the solve_vehicle_routing_problem tool is used from ArcGIS network analysis module and estimated the order count, start and end time in a specific data, total cost, total distance, total travel time etc. and store them in a dataset “Routes_details.csv”.
- Then we find out the delivery addresses of each stores according to their routes and created the dataset as “Stops_details.csv”.
- Then all of the routes of all the stores are visualized in the ArcGIS Map :

![routes](https://github.com/Mainak21/Optimal-Routing-from-Medical-Stores-using-ArcGIS/blob/master/Results/all_routes.png)

## Results

 The routes of all the stores which have that medicine have been shown below :
 
 ### Route 1
 ![route1](https://github.com/Mainak21/Optimal-Routing-from-Medical-Stores-using-ArcGIS/blob/master/Results/Route%201.jpeg)
 
 ### Route 2
 ![route2](https://github.com/Mainak21/Optimal-Routing-from-Medical-Stores-using-ArcGIS/blob/master/Results/Route%202.jpeg)
 
 ### Route 3
 ![route3](https://github.com/Mainak21/Optimal-Routing-from-Medical-Stores-using-ArcGIS/blob/master/Results/Route%203.jpeg)
 
 ### Route 5
 ![route5](https://github.com/Mainak21/Optimal-Routing-from-Medical-Stores-using-ArcGIS/blob/master/Results/Route%205.jpeg)
 
 ### Route 7
 ![route7](https://github.com/Mainak21/Optimal-Routing-from-Medical-Stores-using-ArcGIS/blob/master/Results/Route%207.jpeg)
 
