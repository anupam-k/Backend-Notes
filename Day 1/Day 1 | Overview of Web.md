# _Overview of Web 🌐_

## _Some Points_
- _**Cost of using any package**_ means the _<b>Size that is consumed by the particular package</b>_
- **_Any package that has dependencies_** can be a _**threat to users using that package as some people adds malicious code to get the information**_

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

<b>
  
```javascript
ineuron.ai/courses?
```
</b>

- as soon as you see question mark: means URL query parameter is going to start
- We always have key value Pair

<b>
  
```javascript
ineuron.ai/courses?search_query=Full+Stack+Javascript+Bootcamp
```
</b>
  
- `+` is used to add another key value Pair

<b>
  
```javascript
https://www.youtube.com/watch?v=GdwjE7bqQkY
```
</b>

- when we click a video, it generates a unique id for that specific id

## _API_
- Application Programming Interface
- The user initiates an API call that

## _Node JS Architechture_
- _**Request**_
- _**Node.js Server**_
- _**Event Queue**_
- _**Thread Pool**_
- _**Event Pool**_
- _**External Resource**_

## _Event Pool_
All the requests which are not dependent on anything, then event Loop will execute them

## _Thread Pool_
All the requests which are dependent on anything, they will be sent to Thread Pool and then sent back to Event Pool

![image](https://user-images.githubusercontent.com/91872149/198816568-31c3911f-bc99-46cc-a5aa-ea16a2baa398.png)

## _Workflow of Nodejs Architecture_
- _**Querying for Data**_
- _**Deleteing Data**_
- _**Updating Data**_

## _Server_
- _**Listen**_
- _**Localhost(Domain)**_
- _**PORT (place where a specific Site is placed)**_
- _**A server contains from PORT 0 - 65535**_

![image](https://user-images.githubusercontent.com/91872149/198816640-3db5a418-bc22-4dda-94c6-21ca6730bf3d.png)

## _Application Workflow_
![image](https://user-images.githubusercontent.com/91872149/198816978-27de59ea-8da2-4d39-ab73-6399a0ba8bfb.png)

## _Database_
- _**Structured Query Language(SQL)**_
- _**Not only SQL(NoSQL)(eg.: mongoDB)**_

**_Collections:_** some sort of table kind of format, structure on which we will be entering the value

**_MySQL:_** Primary Key, row(table format)<br>
**_NoSQL:_** Id, Key:value,

## _MVC Architecture_
- _**Model, View, Controller**_

**Use Case of a Resturant**
- **_User:_**   View
- **_Waiter:_** Controller
- **_Chef:_**   Model

## _Middleware_
The middleware in node. js is a function that will have all the access for requesting an object, responding to an object, and moving to the next middleware function in the application request-response cycle.

## _Password Hashing_
<b>
  
`12345 => bcrypt => asdfghyjk`
</b>
- bcrypt changes the normal password to encrypted form

<b>
  
`12345 => bcrypt + salt => asdfghyjkwertyuio`
</b>
- bcrypt=asdfghyjk & salt=wertyuio
