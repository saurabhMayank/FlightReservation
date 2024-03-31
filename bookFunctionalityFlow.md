# Book Functionality Requirement
- User should be able to book flight from any source to any destination on a given date and time
- In case of direct flights are not there, system should book connecting flights from the list shown in search
- In the connecting flight, two seperate tickets for different flights should be booked seperately
- 1 user should be able to book multiple tickets

# Book Functionality System Flow
- User Selects one of the scheduled flight from the list shown
- If flight is direct from source and destination -> then ticket is booked in one flight
- If flight is not direct from source destination -> the ticket is booked in the all the connecting flights
- Ex -> here is taken of cities which have at most 1 intermediary destinations  between
- So in this case two tickets will be booked -> From Source to ID and from ID to destination
- `handle_book_flight` -> function will check if selected scheduled flight is direct from Source to destination
- If yes -> then one ticket will be booked and Booking object will be returned -> for booking ticket -> Also reduce seat capacity in scheduled flight
- If it is connecting then -> two tickets will be booked from From Source to ID and from ID to destination -> Seat capacity reduced in both the scheduled flights
- There is 1 to 1 mapping between Booking Object and Flight. For Connecting Flight -> Multiple Booking Objects will be generated
- <img width="894" alt="Screenshot 2024-03-31 at 12 00 16 PM" src="https://github.com/saurabhMayank/FlightReservation/assets/82028762/79258095-1c75-4bf4-a29a-c4439332a6d5">

