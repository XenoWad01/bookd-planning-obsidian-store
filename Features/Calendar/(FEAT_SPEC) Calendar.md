Needs to fetch a LOT of bookings possibly so _optimize_ it:
- fetch [paginated](https://trpc.io/docs/client/react/useInfiniteQuery) data
- pagination may need to be done by date maybe?
- [optimistic updates for bookings](https://tanstack.com/query/v4/docs/react/guides/optimistic-updates) ( will probably need to put data into more than 1 state so i have it in the most easily accessible format) (if we do this there should only be lag on the initial load. We could also start loading bookings for this from before the user even accesses the calendar. for example start fetching the data from the instant the user is logged in.)


- [How to get html element at (x,y))](https://developer.mozilla.org/en-US/docs/Web/API/Document/elementFromPoint). Get some info from this element, figure out how to progress animations for the timeline progression based on this. Include the date or some shit for example i could encode the date in the key and then do all the animations with springs and bascially it should look kewl.
- alternative is using scroll but idk how that will behave on an ever changing list of items though it could work just fine if i make sure i have the current year + 1 month behind + 1 month forward always loaded. + start loading next / previous year when i get close to a certain treshold. [scroll](https://www.framer.com/motion/use-scroll/) [spring](https://www.framer.com/motion/use-spring/)
- BASICALLY use tanstack virtual, make the get actually a mutation so I can call it programatically. Manage state myself. Do optimistic updates and do smart pagination.
- store state under direct access keys that are formed by date -> item, 
-  scroll-behavior: smooth; obviously
  

- [smooth scrolling with virtual](https://tanstack.com/virtual/v3/docs/examples/react/smooth-scroll)
- [dumbass calendarl](http://react-timeline-9000.s3-website-ap-southeast-2.amazonaws.com/)
- https://codesandbox.io/p/devbox/rhythm-cafe-zfg3tz?file=%2Fsrc%2Fcomponents%2FLevels%2FLevelsList%2FLevelsList.tsx%3A45%2C19