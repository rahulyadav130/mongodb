# We will setup mongoDB authentication-

# list the users-
show user

# list the roles- Roels are applied on database, each database have own roles
show roles
# How we can create a user for a databases (below command will create a user name as rahul with roles add dbs,and full rights)
db.createUser(
 {
   user: "rahul",
   pwd: "sahih",
   roles : [ { role: "userAdminAnyDatabase", db: "admin" }, "readWriteAnyDatabase" ]
 }
)

# Once Userd add, can verify by using below command, it will print all available users for db
show users

# To enable mongodb authentication works, need to enable security in conf file-
open the file /etc/mongod.conf and change configuratoin as  security: enabled
and then restart the services.

# Access mongodb with user name and password -
mondo --host localhost -uadmin -padmin123 
