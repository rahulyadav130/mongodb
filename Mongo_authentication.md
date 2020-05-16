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

