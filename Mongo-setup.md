1. Create a yum repo- /etc/yum.repos.d/mongo.repo

[mongodb-org-4.2]
name=MongoDB Repository
baseurl=https://repo.mongodb.org/yum/redhat/$releasever/mongodb-org/4.2/x86_64/
gpgcheck=1
enabled=1
gpgkey=https://www.mongodb.org/static/pgp/server-4.2.asc

#install mongodb command-
yum install -y mongodb-org

2. { systemctl start mongod; systemctl enable mongod; systemctl status mongod; }
3. mongo # command access mongodb shell access


# if you want to access mongodb db server from remote location
1. edit the conf file "/etc/mongod.conf" and set bindIp: 0.0.0.0 
2. Restart the mongodb service 
{
  systemctl stop mongod
  systemctl start mongod
}  
3. now check you will access mongodb from other location as well.
