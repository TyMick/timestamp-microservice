# Timestamp microservice

I created this app as a requirement for [my freeCodeCamp APIs and Microservices Certification](https://www.freecodecamp.org/certification/tywmick/apis-and-microservices), using [Node.js](https://nodejs.org/en/) and [Express](https://expressjs.com/). The front end API test on the main page also uses [Bootstrap](https://getbootstrap.com/), [jQuery](https://jquery.com/), and [highlight.js](https://highlightjs.org/). The API fulfills the following user stories:

1.  The API endpoint is `GET [project_url]/api/timestamp/:date_string?`
2.  A date string is valid if can be successfully parsed by `new Date(date_string)`.
    - Note that the unix timestamp needs to be an **integer** (not a string) specifying **milliseconds**.
    - In our test we will use date strings compliant with ISO-8601 (e.g. `"2016-11-20"`) because this will ensure an UTC timestamp.
3.  If the date string is **empty** it should be equivalent to trigger `new Date()`, i.e. the service uses the current timestamp.
4.  If the date string is **valid** the api returns a JSON having the structure `{"unix": <date.getTime()>, "utc" : <date.toUTCString()>}` e.g. `{"unix": 1479663089000, "utc": "Sun, 20 Nov 2016 17:31:29 GMT"}`
5.  If the date string is **invalid** the api returns `{"error": "Invalid Date"}`.
