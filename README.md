# FlightResevation LLD
LLD OF flight reservation Platform

# Requirements Section
Requirements of the system Listed

# Use case Diagram Section
Use case Diagrams for the System

# Models
Diagram of all the Models of the system

# API Contracts
All the APIs of the System will be Listed there in the py file

# Class Diagram
Class Diagram of the System

# Design Should answer the following questions
**Question 1**
* Flight can be searched and listed from the platform on the Basis of Date, Time, Source Destination
* Platform needs to list the flight from any Source to any destination, In case there are no direct flights list the connecting flights

**Question 2**
* User should be able to book flight from any source to any destination on a given date and time
* In case of direct flights are not there, system should book connecting flights from the list shown in search
* In the connecting flight, two seperate tickets for different flights should be booked seperately
* 1 user should be able to book multiple tickets

**Question 3** (Little Bit hard question) [Right now not covered, this needs to be covered in the design]
* If Lets Flight A is there, that is going from Source Delhi and Destination Srinagar
* But this flight is also laying over at Delhi
* Means Same Flight from mumbai is going to delhi and srinagar both
* Means In the same flight -> User can go from Mumbai to delhi, Delhi to Srinagar or Mumbai to Srinagar
* How to handle that in the system

