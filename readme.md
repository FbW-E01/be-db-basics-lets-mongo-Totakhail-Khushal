
 db.createCollection("users");
db.users.find();
db.users.insertOne ({_id:1,name:"Veera"});
db.users.find();
db.users.updateOne({"name":"Veera"},{$set:{"name":"Princess Veera Silkenfur"}});
db.users.insert([{"id":2,"name":"Khushal"},{"id":3,"name":"John"},{"id":4,"name":"Khusl"}]);
db.users.updateMany({}, {$set: {professional: true}})



