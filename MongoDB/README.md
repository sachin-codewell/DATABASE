MONGODB

Table - collection
Row - document
Column - field

(case sensitive)
//To show all the databse 
1- show dbs

//To use one databse from all db
2- use <dbname>

//To show all the collections in a db
3- show collections

//TO create a databse 
4.use <dataBaseName> (wiil create databse and will switch to that)

//To see all the data of a collection
4- db.collection.find() or db.collection.findAll()

//To insert a document in collection
5- db.collection.insertOne({name:"sachin",age:23})
   insertOne() is a function takes a json as a parameter.

//To insert many doc at a time
6- db.collection.insertMany([{},{},{},...])
   insertMany() takes array of json as parameter.

// filter data from collection
7- db.collection.find({condition}) exa - db.student.find({section:"A"}) -will return all student of section A.

//using AND ,OR condition
8- db.collection.find({$and:[{cond1},{cond2},..]})
   db.collection.find({$or:[{cond1,{cond2},...]})

//receive limited response from data
8- db.collection.find({}).limit(Number)

//Projection of field - Receive only required fileld in JSON data
8- db.collection.find({},{reuiredField:1,notRequiredField:0})