rest-api-serverless
CRUD api using nodejs, serverless, lambda functions and mongo cluster as Database.


// step 1. Creating a directory


run : sls create -t aws-nodejs -p rest-api && cd rest-api

-->This command will scaffold out all the necessary files and code to create our Lambda functions and API Gateway events. It will do this in the path we gave it with the -p flag. Meaning it will create a directory named rest-api.


// step 2. Installing modules

run : npm install

 -->This will download all your dependencies.

 //step 3. Creating a database on MongoDB Atlas

 https://www.mongodb.com/cloud/atlas?jmp=nav
 
 and setup your cluster and credentials to connect to your database. also download Studio 3T to connect to the database and see the tables.
 
 https://studio3t.com/download/ 

 //step 4.testing with postman.
  run: sls offline start --skipCacheInvalidation

  then go to postman and POST on http://localhost:3000/notes some JSON body with title and description value.
  similarly perform GET, PUT, and DELETE by providing id as endpoint e.g, : http://localhost:3000/notes/some-id

  //step 5. deploy on AWS
  run : sls deploy

  //step 6. To remove functions
  run : sls remove# sreverless-api
