# FETCHAPI ()

* Provides an easier way to handle responses.

`fetch()` method is used to make network requests in the browser. It takes url as input. and handle responses.


- API being used is [dog api](https://dog.ceo/api/breeds/image/random). 

- Fetch uses JS promises to handle results returned from the server. A promise is an evntual result of an async operation.

- They allow us to wait to vertain code to finish execution before running the next bit of code in a cleaner, more readable way.

-We get a response object from the fetch() API promise. We are interested in the body part of the response.

- Promises get executed in sequence. Using a `then ()` method which returns a promise of their own. The methods get executed sequentially once the previous promise if fulfilled.


- **Text doesn't display breed name yet that's because we havn't added options to the select menu** in the HTML its the ```<select><select>``` tag.

- Using API data to populate a select menu at the top of the page. 

- You should not enclose a template literal with brackets.


## Create a Reusable Fetch Function 

You might be required to make a lot of fetch requests such as comments, list of users, list of posts by user.

- Create a resuable data fetching function that runs the fetch, parses, and returns JSON and more all in one place.

- A a wrapper is a function that is intended to call one or more other functions.

- The **fetchData** function returns a  promise that will be resolved/fulfilled once the data is retrieved from the server and parsed to JSON.

- So you chain a **then()** method that updates the new image returned by the API. Takes param data.

- Once, the fetch promise is fulfilled, it returns a response object containing information about the response.

-Fetch is only concerned with sending a request and receiving a response from the server, we should also provide a way of checking for and handling failed HTTP responses. 


- `Promise.all` is an all or nothing operation, hence it will reject as soon as one of the passed params are rejected.

## Posting Data with `fetch()`.


- The default HTTP method for making fetch requests is GET, which retrieves data from a server. You can make requests other than GET (like POST, DELETE, and PUT) by passing additional information to fetch().

- Create a function that uses fetch to post the name and comment form data to a server on submit.
