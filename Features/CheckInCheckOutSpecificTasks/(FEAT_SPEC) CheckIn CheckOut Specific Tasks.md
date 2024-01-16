
# Backend implications

```ts
interface Room {}
interface Date {}
getCheckinCheckoutData(fromDate: Date, toDate: Date): {
		checkInData: Array<{
			clientName: string, 
			nightsToSpend: number, 
			payedForCheckInTransport: boolean,
			status: string
			room: Room, 
			checkOutDate: Date
		}>,
		checkOutData: Array<{
			clientName: string, 
			nightsToSpend: number, 
			payedForCheckOutTransport: boolean,
			status: string,
			room: Room, 
			checkInDate: Date
		}>
} => ( /* whatever */)
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