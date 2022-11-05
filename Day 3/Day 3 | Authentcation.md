# _Revise Concepts_
- Express
- Request and Response
- How to send the response
- PORT
- Nodemon
- POSTMAN
- API (making)
- Status Code
- Web Request

# _Topics for Today_
<b>Topic 1:</b> Quick Over<br>
<b>Topic 2:</b> process.env and dotenv<br>
<b>Topic 3:</b> ORM and ODM<br>
<b>Topic 4:</b> Biagram B-Logic<br> 
<b>Topic 5:</b> Functionality<br>

<br>

<b><i>Create Account</b></i> => name, email, mobile , pass<br>
<b><i>Login</b></i>          => email and Pass<br>
<b><i>Course Buy</b></i>    => user id, cid, price, paymentgateway<br>
<br>
- How to make things permannt
- How to Inject Database
- Hide Secret
   - HMAC
   - SHA256
- Handle a particular ROUTES

## _process.env_
- The process.env property returns an object containing the user environment

## _dotenv_
- Everything that are credentials, those are written in dotenv file.
- It is zero dependency module
- .env doesn't allow semi-colon
- .env must be in root directory

## _Mongodb_
- We will be choosing `Mongodb`

 **Object Relational Mapping(ORM)** - SQL and <br>
 **Object Document Mapping(ODM)** - No SQL

## _Mongoose_
- **_Mongoose is ODM for Mongodb_**
- **_Tool which makes communication easier_**

![image](https://user-images.githubusercontent.com/91872149/200102464-2b07e164-44d9-485f-a6dc-6e6edcd375b7.png)

## _Q. Why nodemon is install as dev dependency_

Dev dependencies like nodemon we don't want to package for final build of the application. These are only for development purpose to run the application on local

## _Steps_
**_1) npm init_**<br>
**_2) Required tool installation: express dotenv and mongoose_**<br>
**_3) Dev (nodemon)_**<br>
**_4) Design Schema for User_**<br>
**_5) From the User_**<br>
       &nbsp;&nbsp;&nbsp;&nbsp;- _Get all information_<br>
       &nbsp;&nbsp;&nbsp;&nbsp;- _Check Mandatory_<br>
       &nbsp;&nbsp;&nbsp;&nbsp;- _Check Email Unique_<br>
       &nbsp;&nbsp;&nbsp;&nbsp;- _Take care of Password_<br>
       &nbsp;&nbsp;&nbsp;&nbsp;- _Success Message or Send Token_<br>

## _Database design: Homework_
- Customer ecommerce
- Normal user
