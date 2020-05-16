# mongodb
list the available dbs
# Check the db serer status
db.stats() 
# show dbs
to switch in Database
# use admin or use dbname
db.stats() 

# Create a fresh DB
“ use DNMAME”


# print all available collections
show collections

# Delete the collectoin
db.movies.drop()

# Insert data in collection----
	db.os.insert(
...  {
...    "Windows": "Windows 2008",
...    "Windows": "Widnows 2016",
...    "linux" : "Centos"
... }
... )
# Show collectoin
os
>  db.os.find()
{ "_id" : ObjectId("5ebef9fd68827f481bcd8ab7"), "Windows" : "Widnows 2016", "linux" : "Centos" }
###### 
> db.os.find().pretty()
{
	"_id" : ObjectId("5ebef9fd68827f481bcd8ab7"),
	"Windows" : "Windows 2016",
	"linux" : "Centos"
}

#### Update document in exising collection-
db.os.update({"Windows":"Widnows 2016"}, {$set: {"monbilekaos":"Android"}})
WriteResult({ "nMatched" : 1, "nUpserted" : 0, "nModified" : 1 })

# we can verify if updated document is available or not 
db.os.find().pretty()
{
	"_id" : ObjectId("5ebef9fd68827f481bcd8ab7"),
	"Windows" : "Windows 2016",
	"linux" : "Centos",
	"macos" : "OSx",
	"monbilekaos" : "Android"
#############################################################
# Update or delete records from exising collectoin (We are deleting a key-pair"monbilekaos":"Android" from db.os)
db.os.update({"Windows":"Widnows 2016"},{$unset: {"monbilekaos":"Android"}})
WriteResult({ "nMatched" : 1, "nUpserted" : 0, "nModified" : 1 })

# with reference above command we can verify a key-pair"monbilekaos":"Android" has been deleted from db.os)
db.os.find().pretty()
{
	"_id" : ObjectId("5ebef9fd68827f481bcd8ab7"),
	"Windows" : "Widnows 2016",
	"linux" : "Centos",
	"macos" : "OSx"
}

# Query (print the collectoin with specific key)
db.os.find({"released":"2000"}).pretty()

# Query (print the collection with ignore "_id")
db.os.find({},{"_id":0}).pretty()

