
# Backend implications

```
getCheckinCheckoutData(fromDate, toDate) => ({
	checkInData: [{
		clientName: string, 
		nightsToSpend: number, 
		room: room, 
		checkOutDate Date, 
		payedForCheckInTransport: bool,
		status: string
	}], 
	checkOutData: [{
		clientName, 
		nightsToSpend, 
		room, 
		checkInDate, 
		payedForCheckOutTransport: bool
		status: string
	}]
})
```
- For checkin ones: Bookings that have startDate today and have status AWAITING_START OR IN_PROGRESS
- For checkout: Bookings that have endDate today and have status IN_PROGRESS

# Frontend implications

- We will have 2 tables with booking data to show: 
	- CheckIn
	- CheckOut

## OLD UI Visualization: 


![[Features/CheckInCheckOutSpecificTasks/(PIC) CheckInCheckOutSpecificTasks-OLD.png]]


![[Features/CheckInCheckOutSpecificTasks/(PIC) CheckInCheckOutSpecificTasks-OLD-Filter.png]]