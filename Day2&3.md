Mongodb commands - 

	use dbName

	db.collectionName.insertOne( { x: 1 } ) || db.myNewCollection3.createIndex( { y: 1 } )
	
	we can create collection with validation like this - 
	
	//validations
	db.createCollection("students", {
	   validator: {
		  $jsonSchema: {
			 bsonType: "object",
			 title: "Student Object Validation",
			 required: [ "address", "major", "name", "year" ],
			 properties: {
				name: {
				   bsonType: "string",
				   description: "'name' must be a string and is required"
				},
				year: {
				   bsonType: "int",
				   minimum: 2017,
				   maximum: 3017,
				   description: "'year' must be an integer in [ 2017, 3017 ] and is required"
				},
				gpa: {
				   bsonType: [ "double" ],
				   description: "'gpa' must be a double if the field exists"
				}
			 }
		  }
	   }
	} )
	
	
	we can have views in mongodb similar to mysql


Basic CRUD -
	
	show collections
	
	db.createCollection()
	
	db.collection.drop()
	
	db.collection.insertOne({field:"value"})
	
	db.collection.insertMany()
	
	db.collection.find()
	
	db.collection.updateOne()
	
	db.collection.findAndModify()
	
	db.collection.findOneAndUpdate()
	
	db.collection.findOneAndReplace()
	
	db.collection.deleteOne()
	
	db.collection.deleteMany()
	
	
	cursor.explain("executionStats") 
	
	Studied different syntaxes to querry over array , embedded doc, array of embeded document
	upsert : true - if dont find matching condition then it will create new doc.
	
	
	
	
Data models - 

	Access pattern
	Document structre - 
		Embeded - 1:1 or 1:many
		Reference - use if data duplication or data anomalise is there, many:many relations, 	use&lookup to join such collection
	
	Schema validation
	
Indexing -

	for faster querry of read operation
	inserting takes time.
	without indexing find operation scan all the document .
	compund index , text index
	

Transaction -

	While updating many documents in single querry, the whole update process is not atomic but the single update is atomic.
	
Sharding - 

	horizontal scaling
	it just adding more servers.
	Partition of data happens between server.
	
	
Aggregation framework -

	use to group the document and performing operation over that collection.
	$match 
	$group
	$count 
	$sort
	$project
	$limlit
	$unwind - works with array
	Accumlators - sum,avg,max
	Unary operator - $type,$lt,$and,$or,$gt,$multiply
	
