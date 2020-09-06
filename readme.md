# Docker Compose MongoDB for Developer

## Run Docker Compose

### build images

 `$ docker-compose -f docker-compose.yml build --force-rm`

### run

`$ docker-compose -f docker-compose.yml up`

### docker exec

`$ docker exec -it mongodb_mongodb_container_1 bash`

## MongoDB credential (for database `admin`)

- Username: root
- Password: rootpassword

## How to connect to MongoDB

### Via mongo Shell

#### Type this

`$ mongo admin -u root -p rootpassword`

It will connect to localhost port 27017.

Note that `mongo` command should be installed on the computer. On Linux this should be install `mongodb-org-shell` only. Refer to this for more detail https://docs.mongodb.com/manual/installation/

## Some quick tips after logged-in

Show databases:

`$ show dbs`

Create new non-existant database:

`$ use mydatabase`

Show collections:

`$ show collections`

Show contents of a collection:

`$ db.your_collection_name.find()`

Save a data to a collection:

`$ db.your_collection_name.save({"name":"Sony AK"})`

Show database version:

`$ db.version()`

Enjoy your local MongoDB database server for any purpose you want, for me this setup is fine for testing purpose.