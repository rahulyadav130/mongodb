# There is many way to take mongo db dump, so lets look backup process---

# mongodb Backup and restore
# mongo DB full backup
mongodump 
# mongodump takes all db full dump

# You can also, specify output directory
mongodump --out /tmp/fulldump
# You can also take specific DB-
mongodump --db dbname

# You can also take specifc DB and specific collection dump--
mongodump --db test --collection os --out /tmp/onlyos_collection

# Now lets look restore process
# in this example we are restoring backup into other VM-... So lets copy copy the backup file and then restore.
# restore command-
mongorestore backupfilename
