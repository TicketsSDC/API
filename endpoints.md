# Endpoints

None of these endpoint descriptions specify any of their parameters or authentication requirements. They are merely a starting point before a more thorough API specification is written.

Any data being transmitted over the calls will be in [JSON](http://json.org). No XML.

#### Ticket endpoints:

HTTP Verb | URL Endpoint | Description
----------|----------|------------
`POST` | `/api/v1/tickets/` | Create a ticket, returns new ticket's data
`GET` | `/api/v1/tickets/TICKET_ID` | Return data for a specific ticket
`PUT` | `/api/v1/tickets/TICKET_ID` | Modify the ticket with the given ID
`DELETE` | `/api/v1/tickets/TICKET_ID` | Delete the ticket with the given ID


#### Bid endpoints:

HTTP Verb | URL Endpoint | Description
----------|----------|------------
`POST` | `/api/v1/bids/` | Create a bid, returns new bid's data
`GET` | `/api/v1/bids/BID_ID` | Return data for a specific bid
`PUT` | `/api/v1/bids/BID_ID` | Modify the bid with the given ID
`DELETE` | `/api/v1/bids/BID_ID` | Delete the bid with the given ID


#### Event endpoints:

The event endpoints are missing some verbs (like `POST`, `PUT` and `DELETE`) because event objects are unique enough that they can be manually entered into the database by the developers.

HTTP Verb | URL Endpoint | Description
----------|----------|------------
`GET` | `/api/v1/events/` | Return list of all events
`GET` | `/api/v1/events/EVENT_ID` | Return data for a specific event
`GET` | `/api/v1/events/EVENT_ID/stats` | Return a collection of aggregate ticket, bid and event statistics
`GET` | `/api/v1/events/EVENT_ID/tickets` | Return list of all tickets for a specific event
`GET` | `/api/v1/events/EVENT_ID/bids` | Return list of all bids for a specific event
