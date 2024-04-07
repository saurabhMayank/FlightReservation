# User Booking Mutliple Seats
* Now I am a user, I can book mutliple seats
* It is possible that I may not  book seats for myself
* So a User can book multiple Seats but that seat is associated to seperate Users
* What is common in all these tickets is the Booking Id or PNR status
* No matter How many seats a users book, it will be associated to different Users but it will have same PNR status or booking ID
* So there should be a ticket Class -> Ticket class should have booking Id and User Instance
* 1 Booking Model is connected to mutliple ticket models

# Flight having Layover
* The Design is currently not addressing the question altogether completely
* Need to incorporate the Design in the system for this
* Lets say there is a flight which has Source as Mumbai, Destination as Srinagar but it is also laying over in delhi
* Layover is restricted to One Hop for now -> for simplicity of the Design
* In this case -> Treat all the routes as different schedules
* Mumbai to Delhi -> One schedule, Mumbai to Srinagar -> One Schedule, Delhi to Srinagar -> One Schedule
* One Flight can be mapped to multiple schedules on a single day
* There should be a mapping of schedule and Seat available for that flight -> In the schedule Model
* If I book a set in the flight in Mumbai to Srinagar Schedule
* For that flight there should be also be updation of seat capacity in Mumbai to Delhi and Delhi to srinagar schedule for the same flight
* On the basis of Flight instance and day -> we can fetch which schedule have same flights

# Remove time from the design
* Remove time from the design -> it is not needed
