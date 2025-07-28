src = https://www.youtube.com/watch?v=PTfZcN20fro

# Intro

**REST** = REpresentational State Transfer  
**GraphQL** = Graph Query Language  

Both REST and GraphQL are use to build **APIs** = Application Programming Interfaces.  
Those allow different applications to communicate with each other over the Internet.  

An API takes requests from a **client**, which can be a web application or a mobile app.  
Then it retrieves the requested data from a **server**.  
And finally, it sends the data back to the client.  

GraphQL and REST are 2 different approaches to building APIs.
- GraphQL prioritizes, giving clients exactly the data they request, and no more
- REST is more "talkative", often providing more information than needed

# REST

REST is an architectural style that relies on HTTP requests to interact with resources.  

## Resources

They are the fundamental concept in REST,  
Each resource has a unique identifier called a URI = Uniform Resource Identifier  

A client can request access to a resource using an HTTP method:
- GET
- PUT
- POST
- DELETE

The server will respond with a representation of the resource in a format like JSON or XML.  

REST also allows clients to filter, sort, and paginate the data using query parameters.  

# GraphQL

GraphQL is a query language that allows clients to retrieve data from multiple data sources in a single API call. 
With GraphQL, we can build a single API endpoint that allows clients to query of all the data in a single request.  

- Clients must specify exactly the data that they need
- the server uses a set of resolvers to fetch the necessary data from each source
- then the multiple responses get assembled into a single response that matches a specific schema  

## Schema

In GraphQL, we have something called a "**schema**".  
This is the blueprint that defines all the posisble data that clients can query through a service.  

## Query

A query is a request for data that follows the structure defined in the schema.  

## Resolver

The resolver is called to retrieve the data requested in the query.  
This may involve fetching data from multiple data sources and assembling it into a response.  
That response must match the query structure.  

## Mutations 

Their job is to modify data on the server.  

If we think of this in terms of the CRUD model (CREATE, READ, UPDATE, DELETE):
- a query would be equivalent to the READ functionality
- all the others are handled by the **mutations**

# How are GraphQL and REST similar?

- They are both used to build **APIs**, which allow applications to communicate over the Internet
- For that communication to happen, they both use **frameworks** and **libraries** to handle all of the networking details
- They also both operate over **HTTP**, even though GraphQL is actually **protocol-agnostic**
- Both can handle requests and responses using JSON (JavaScript Object Notation)

**Protocol-agnostic** means that GraphQL is not tied to any specific network protocol for communication between client and server.  

# Key differences between these 2 technologies

REST APIs often require multiple requests to fetch related data, while GraphQL can fetch all the data in a single request.  
To achieve that, GraphQL uses complex queries that follow a schema, as mentioned earlier.  

REST APIs are well-suited for applications that require simple CRUD-like operations.  
GraphQL is better suited for applications that require a bit more complex data requests (nested fields, multiple data sources).  

# Combining them

REST and GraphQL can also work together because GraphQL doesn't dictate a specific application architecture.  
GraphQL can be introduced on top of an existing REST API, and can also work with existing API management tools.  
