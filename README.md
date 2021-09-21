# Backend - Database - Basics - Let's MonGO

## Let's monGO

Add your answers directly into this README file.

1. Explain ObjectIDs in MongoDB; what are they?

An ObjectID is a 12-byte Field Of BSON type. The first 4 bytes representing the Unix Timestamp of the document. The next 3 bytes are the machine Id on which the MongoDB server is running. The next 2 bytes are of process id. The last Field is 3 bytes used for increment the objectid.`

2. You have a collection called "users" with a document like this: `{ _id: 1, name: "Veera" }`. What query would you use to update the name to "Princess Veera Silkenfur"?

db.users.updateOne({"name":"Veera"},{$set:{"name":"Princess Veera Silkenfur"}});

3. How do you make a collection?

db.createCollection("users");

4. So the (old) mongo shell is kind of like a JavaScript REPL. What is a REPL? Which other REPL have we used?

(REPL) is an interactive shell that processes Node.js expressions. The shell reads JavaScript code the user enters, evaluates the result of interpreting the line of code, prints the result to the user, and loops until the user signals to quit.
we have used
Node.js v15.11.0.
mariadb.
mongo.

5. So the (old) mongo shell is kind of like a JavaScript REPL. You can use things like variables, try...catch statements and loops. Experiment with it and find at least three other JavaScript things that we have used that work in the (old) shell. If you can, try to find even more!
Read Evaluate Print Loop, 
function out(x) { print("Hello " + x); }` 

6. (Research) So the old shell is pretty cool. How is the new shell better?

Improved syntax highlighting.
Improved command history.
Improved logging.
To maintain backwards compatibility, the methods that mongosh supports use the same syntax as the corresponding methods in the mongo shell.

7. (Research) How can you insert multiple documents at the same time?

db.users.insertMany(
    {"id":2,"name":"Khushal"},
    {"id":3,"name":"John"},
    {"id":4,"name":"Khusl"});

8. (Research) You have a collection called `cats` with a documents like this: `{ name: "Veera" }, { name: "Rauli" }, { name: "BenBen" }` - How can you insert the field `cute: true` into all of them with one command?

db.users.updateMany({}, {$set: {professional: true}})

9. (Task) Start a timer for 30 minutes. Spend all that time getting to know and reading https://docs.mongodb.com/manual/introduction/ - how far did you get? What was the most cool or interesting thing you learned?

10. Find one SQL Cheatsheet and one MongoDB Cheatsheet and add links to them here.
    https://www.sqltutorial.org/sql-cheat-sheet/
    https://dzone.com/articles/mongodb-commands-cheat-sheet-for-beginners
    https://dzone.com/articles/mongodb-commands-cheat-sheet-for-beginners

🌿
