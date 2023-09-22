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
4- db.collection.find() or db.collection.findAll() or db.collection.finOne({})

//To insert a document in collection
5- db.collection.insertOne({name:"sachin",age:23})
   insertOne() is a function takes a json as a parameter.

//To insert many doc at a time
6- db.collection.insertMany([{},{},{},...])
   insertMany() takes array of json as parameter.

// filter data from collection
7- db.collection.find({condition}) exa - db.student.find({section:"A"}) -will return all student of section A.

//receive limited response from data
8- db.collection.find({}).limit(Number)

//Projection of field - Receive only required fileld in JSON data
8- db.collection.find({},{reuiredField:1,notRequiredField:0})

//To count the number of documents in row
9- db.collection.count()

//To receive the res in the form of array
10- db.collection.find({}).toArray() - will return the array of json.
cant use it with findOne().

//To sort the response in ascending or descending order.
11- db.collection.find().sort({field:-1 OR ,field:1})
    if field:-1 will sort data in descending order on te basis of given field value
    if field:1 will sort data in asceending order on te basis of given field value

//To delete document from coleection
12- db.collection.deleteOne({field:value}) - will delete one matching record
    db.collection.deleteMany({field:value}) - will delele all matching record

//To update the record or row in collection
13- db.collection.updateOne({matchinCondition},{$set:{filed1:value1,filed2:value2}})  
    db.student.updateOne({id:123},{$set:{name:"Sachin",company:"Want to switch"}})  
    db.collection.updateMany({expression},{$set:{}}) - same as updateOne() but will update all matching data.

-----------------------------------OPERATORS----------------------------------------------
//using AND ,OR operator
8- db.collection.find({$and:[{cond1},{cond2},..]})
   db.collection.find({$or:[{cond1,{cond2},...]})
   Example - db.student.find({$and:[{age:{$lt:20}},{age:{$gt:15}}]})

//!=($ne), <($lt), >($gt), ==($eq), <=($lte), >=($gte) operator
14- db.collection.find({Score:{$lt:33}}) return all record having Score<33
   db.collection.find({Score:{$gt:85}}) return all records having Score>85
   db.collection.find({Score:{$ne:0}})  return all record except Score==0
   db.collection.find({Name:{$eq:"Sachin"}})



