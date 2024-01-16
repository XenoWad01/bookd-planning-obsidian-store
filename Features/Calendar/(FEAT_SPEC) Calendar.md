Needs to fetch a LOT of bookings possibly so _optimize_ it:
- fetch [paginated](https://trpc.io/docs/client/react/useInfiniteQuery) data
- pagination may need to be done by date maybe?
- [optimistic updates for bookings](https://tanstack.com/query/v4/docs/react/guides/optimistic-updates)
- use [@tanstack/table](https://tanstack.com/table/v8) and [@tanstack/virtual]() (useful examples):
	- [smooth scrolling with virtual](https://tanstack.com/virtual/v3/docs/examples/react/smooth-scroll)