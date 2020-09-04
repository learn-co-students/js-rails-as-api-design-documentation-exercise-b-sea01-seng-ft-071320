# README

This is an API to get coffee. Got your mug?

The endpoint for this API is `http://localhost:3000/coffee`

There are two queries you can attach to the path and one modifying query: `origin` and `limit`

`origin` will only serve coffees that match the origin string passed to the query

Here's an example:

`http://localhost:3000/coffee?origin=jamaica`

`limit` will limit the results to the number passed to the query

* Optionally, you can include `page` to a `limit` query (where page 0 is the first page) to paginate the results based on the limit number. _without the page query, limit will always return the first page of results_

As examples:

`http://localhost:3000/coffee?limit=50`

`http://localhost:3000/coffee?limit=100&page=2`

_remember that this second path actually gets the **third** page of results_

You can also combine all of these queries in one request in no particular order:

`http://localhost:3000/coffee?origin=jamaica&limit=50&page=0`

Have fun!
