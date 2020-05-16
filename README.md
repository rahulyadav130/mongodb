# mongodb
list the available dbs
Check the status of Database server
db.stats() 
# show dbs
to switch in Database
# use admin or use dbname
db.stats() 

create a fresh db 
“ use DNMAME”


#print the all available collection
show collections

Delete the collection 
db.movies.drop()

#### Insert data in collection----
	db.os.insert(
...  {
...    "Windows": "Windows 2008",
...    "Windows": "Widnows 2016",
...    "linux" : "Centos"
... }
... )
> show collections
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






