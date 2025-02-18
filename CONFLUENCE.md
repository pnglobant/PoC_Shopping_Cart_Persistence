# Shopping Cart State Management

We successfully created a shopping cart simulating the whole flow that is currently depicted in Figma using Next.js 15/React 19. Code can be found in [https://github.com/ericmaya8a/merlin-ticket-poc](https://github.com/ericmaya8a/merlin-ticket-poc). For this we used the localStorage (or sessionStorage, depending on the need) as a store of sorts. In it we saved all data that was relevant to the flow: 
- data related to visit: date of visit, adults/children
- basket information (summary, total cost, etc)
- extras selected by user
- T&C agreement, etc

We didn't find any issues in completing the flow from end to end while persisting the pertinent data in each step of the flow as simple jsons stringified. Storage limit (5mb) shouldn't be an issue at all, as we're far from that value, and also we clean it up in the last step. Note: we might want to sanitize the content stored in the localStorage/sessionStorage (as it's stored as strings) just in case of any malformed/corrupted data.

To simplify reading/writing to the localStorage we used [https://usehooks-ts.com/react-hook/use-local-storage](https://usehooks-ts.com/react-hook/use-local-storage)
