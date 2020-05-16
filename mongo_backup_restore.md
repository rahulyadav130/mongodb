# there is many way to take mongo db dump, so lets look backup process---

# mongodb Backup and restore
# mondo DB full backup
mongodump 
# mongodump takes all db full dump

# you can also, specify output directory
mongodump --out /tmp/fulldump
# you can also take specific DB-
mongodump --db dbname

# you can also take specifc DB and specific collection dump-
mongodump --db test --collection os --out /tmp/onlyos_collection
