# Backend implications:
- `getCurrentOccupancyStats(fromDate: Date, toDate: Date)`:
	- We take the occupancy at request time for all bookings that are in progress.(for all rooms -> for all bookings that are in progress and have at least one PetInRoom tied to this booking and room). We track free vs occupied rooms. A room is occupied if it has at least one pet in it.
	- Do this but filter for all bookings by from and to date to get relevant results
# Frontend implications:
### Old stuff
![[(PIC) CheckInCheckOutSpecificTasks-OLD.png]]
![[(PIC) CurrentOccupancyFeature-OLD.png]]![[(PIC) CheckInCheckOutSpecificTasks-OLD-Filter.png]]
### New stuff:

- Create Booking BUTTON:
	- redirects to calendar / scrolls to current day
- Create Client BUTTON:
	- opens create client modal