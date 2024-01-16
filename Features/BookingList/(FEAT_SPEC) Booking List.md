# Backend implications
```
getBooking({
	status: array of 'IN_PROGRESS' | ''.... all of em
}) ( will be paginated )
```
https://trpc.io/docs/client/react/useInfiniteQuery  for pagination

# Frontend implications
- Will literally show a list of bookings
- Will have like 5 buttons for each status that will represent booleans(turn on/off) and will make call with all of the status names that are turned on 