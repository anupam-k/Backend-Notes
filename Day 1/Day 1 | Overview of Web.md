# _Overview of Web 🌐_

## _Some Points_
- Cost of using any package means the size that the particular package is consuming
- Any package that has dependencies can be a threat to users using that package as some people adds malicious code to get the information

# _Topics_
- _**How to Integrate Frontend to Backend**_
- _**Authentication**_
- _**Building API**_
- _**Building E-commerce Application**_
- _**Building a Social Media Application**_
- _**Best Practices**_

## _Write an Article on V8 📖_
- _**Write an in-depth Article**_
- _**What is is**_
- _**Why it is being Used**_
- _**What is it capable of**_

## _Connecting the Dots_

## _Now we can watch:_ _Pro Backend Course_

# _Backend_

## _Tools of Backend Developers_
- _**Node JS**_
- _**Postman**_
- _**Express JS**_

## _How Internet Works?_
- _**Request**_
- _**Response**_
- _**URL Query/URL String**_

```javascript
ineuron.ai/courses?
```

- as soon as you see question mark: means URL query parameter is going to start
- We always have key value Pair

```javascript
ineuron.ai/courses?search_query=Full+Stack+Javascript+Bootcamp
```

- `+` is used to add another key value Pair

```javascript
https://www.youtube.com/watch?v=GdwjE7bqQkY
```

- when we click a video, it generates a unique id for that specific id

## _API_
- Application Programming Interface
- The user initiates an API call that

## _Node JS Architechture_
- Request
- Node.js Server
- Event Queue
- Thread Pool
- Event Pool
- External Resource

## _Event Pool_
All the requests which are not dependent on anything, then event Loop will execute them

## _Thread Pool_
All the requests which are dependent on anything, they will be sent to Thread Pool and then sent back to Event Pool

![image](https://user-images.githubusercontent.com/91872149/198816568-31c3911f-bc99-46cc-a5aa-ea16a2baa398.png)

## _Workflow of Nodejs Architecture_
- Querying for Data
- Deleteing Data
- Updating Data

## _Server_
- Listen
- Localhost(Domain)
- PORT (place where a specific Site is placed)
- A server contains from PORT 0 - 65535

![image](https://user-images.githubusercontent.com/91872149/198816640-3db5a418-bc22-4dda-94c6-21ca6730bf3d.png)

## _Application Workflow_
![image](https://user-images.githubusercontent.com/91872149/198816978-27de59ea-8da2-4d39-ab73-6399a0ba8bfb.png)

## _Database_
- Structured Query Language(SQL)
- Not only SQL(NoSQL)(eg.: mongoDB)

**_Collections:_** some sort of table kind of format, structure on which we will be entering the value

**_MySQL:_** Primary Key, row(table format)<br>
**_NoSQL:_** Id, Key:value,

## _MVC Architecture_
- Model, View, Controller

**Use Case of a Resturant**
- **_User:_**   View
- **_Waiter:_** Controller
- **_Chef:_**   Model

## _Middleware_
The middleware in node. js is a function that will have all the access for requesting an object, responding to an object, and moving to the next middleware function in the application request-response cycle.

## _Password Hashing_
`12345 => bcrypt => asdfghyjk`
- bcrypt changes the normal password to encrypted form

`12345 => bcrypt + salt => asdfghyjkwertyuio`

- bcrypt=asdfghyjk & salt=wertyuio
