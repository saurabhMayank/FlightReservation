# Search Functionality Requirement
- User Should be able to search a flight based on Source, Destination, Date, Time
- The system should show all the flights which are scheduled from the required Source to required Destination


# Search Functionality System Flow
- User enters the Source, Destination, Date, Time on the platform
- The functionality internally calls the `search_flight` API
- `search_flight` internally calls `show_flights` in Display service
- <img width="922" alt="Screenshot 2024-03-30 at 7 04 07 PM" src="https://github.com/saurabhMayank/FlightReservation/assets/82028762/5bce7488-e20e-4502-bf4a-456482d8a353">
- `show_flights` queries the Schedule Model based on source, destination, date and time for all flights with `flightStatus=scheduled`
- If between a source and destination direct flights are not found
  - In that case Display Service fetches all the flights originating from Source at given date and time from schedule model
  - Treat all the intermediary destination as sources and find flights originating from these IDs after flight from Source has reached the IDs
  - For Example Source A has 4 flights going to F1 -> ID1, F2 -> ID2, F3 -> ID3, F4 -> ID4
  - From ID2 -> F5 goes to destination B and From ID3 -> F6 goes to destination B
  - F5 goes to destination B after F4 has reached -> So system will list that flight as an option
  - Can also code this if required -> Ask neetesh if needed
  - After that list them down
  - <img width="835" alt="Screenshot 2024-03-30 at 7 24 39 PM" src="https://github.com/saurabhMayank/FlightReservation/assets/82028762/e1e62095-570a-409a-b100-b8eb77a49cef">

- Search Functionality 

  


