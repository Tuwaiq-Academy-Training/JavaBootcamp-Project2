Car Pooling System is an application that helps managing cars scheduling and bookings. The system consists of Cars, Routes and Passengers.

- Car Class has: a code, a fixed route, a maximum capacity of passengers per trip.

- Route Class has: start pick up address, destination address, and trip price. 

- Passenger (parent class) has: name, ID, reserved Car object, trip cost.
Also, it has an abstract function that takes a car object to reserve it to the passenger and compute the trip cost and a function that should be overridden to display their information along with the car code and route price.

There are two types of Passengers (subclasses):

- Subscribers passengers: take 50% discount on trip cost when they reserve a car.

- Non-Subscribers passengers: have boolean value named discount coupon and gets a 10% discount on the trip cost if they have it.

The function that reserves a car and calculates the trip cost uses the following equation:

Trip cost = car_object.route_object.price - (car_object.route_object.price 0.1) --> in case the Non-Subscribers passengers has a discount coupon.

Trip cost = car_object.route_object.price --> in case the Non-Subscribers passengers doesn't have a discount coupon.

Note that: 
The function used to reserve a car to a passenger should throw an exception if the maximum capacity of the car was equal to zero In.

---------------------------------

In the main function do the following:
- Create 2 routes and assign each of them to a different Car object. Note that one of those cars should have a maximum capacity equals zero.
- Create an array of Passengers containing 1 Subscriber and 1 non-Subscriber.
- Assign a different car object to each passenger and then display their information.
