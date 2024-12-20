# last_mile_delivery
## Optimize last mile delivery for an e-commerce

Amazon's main operational challenge is last-mile delivery; it can be complex and costly.

As a data scientist, what can you do?

If you travel to first and second-tier cities of USA, you will find on the street many delivery drivers.

They take the parcels from Amazon's warehouses called customer service centres  located in each neighbourhood and deliver them to the final customers.

They provide extensive geographical coverage for last-mile delivery to offer the best service level and delivery lead time in the market.

How can you use Python to optimize the routing from these centres?

This project will present a solution to optimize the last-mile delivery from these centres, reducing costs and ensuring a uniform workload distribution to each driver.

I. How to optimize last-mile delivery with Python?
  1. Problem Statement: Last Mile Delivery Optimization
  2. Distance Matrix
  3. Demand: number of parcels to deliver to each location
II. Build your Model
  1. Import Distance Matrix and Init parameters
  2. Create functions to calculate distances and order quantities
  3. Build your model with constraints
  4. Show the solution

Optimize last-mile delivery with Python
Problem Statement: Last Mile Delivery Optimization
You are a Supply chain Analyst at Amazon.

The operational manager in a local service centre requested your support to manage his fleet.

### Constraints

Four drivers in his team
15 parcel capacity per vehicle
16 destinations to cover in the neighbourhood named Dj with j in [1, 16]
D0 is the centre
One route per driver

What are the parameters?

Distance Matrix
To build your model, you need to provide a distance matrix M as inputs defined by

M(i, j) with i, j in [0, 16]
M(i, j) = distance between Di and Dj
This distance matrix will be loaded from a CSV file.

They represent all the locations we must cover in the centre's scope.

What about the volumes of parcels?

Demand: number of parcels to deliver to each location
We will use here a Python list with the first value at zero (because you don’t provide anything in the centre)

Demand = [0, 1, 1, 2, 4, 2, 4, 8, 8, 1, 2, 1, 2, 4, 4, 8, 8]



Objective

Deliver all parcels with a minimum number of drivers
Optimize the routing to minimize the distance covered per route


Results



100% of parcels are delivered with a minimum distance covered
Drivers’ vehicles are loaded to their maximum capacity (15/15)


What are the benefits?

Using this model helps ensure that your drivers, who are paid a fixed amount by delivery, will be fairly assigned to a route.
You will avoid the issue of having drivers complaining because they have longer routes than their colleagues.
Moreover, you are using your resources at their maximum capacity.


Conclusion

This model can help the centre manager to
Optimize his fleet with full utilization of his drivers and vehicles
Ensure that the workload is equally distributed among each driver