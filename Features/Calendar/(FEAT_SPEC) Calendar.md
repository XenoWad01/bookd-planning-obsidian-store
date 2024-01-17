Needs to fetch a LOT of bookings possibly so _optimize_ it:
- fetch [paginated](https://trpc.io/docs/client/react/useInfiniteQuery) data
- pagination may need to be done by date maybe?
- [optimistic updates for bookings](https://tanstack.com/query/v4/docs/react/guides/optimistic-updates) ( will probably need to put data into more than 1 state so i have it in the most easily accessible format) (if we do this there should only be lag on the initial load. We could also start loading bookings for this from before the user even accesses the calendar. for example start fetching the data from the instant the user is logged in.)


- BASICALLY use tanstack virtual, make the get actually a mutation so I can call it programatically. Manage state myself. Do optimistic updates and do smart pagination.
- store state under direct access keys that are formed by date -> item, 
  

- [smooth scrolling with virtual](https://tanstack.com/virtual/v3/docs/examples/react/smooth-scroll)
- [dumbass calendarl](http://react-timeline-9000.s3-website-ap-southeast-2.amazonaws.com/)
- https://codesandbox.io/p/devbox/rhythm-cafe-zfg3tz?file=%2Fsrc%2Fcomponents%2FLevels%2FLevelsList%2FLevelsList.tsx%3A45%2C19