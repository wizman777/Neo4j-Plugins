## Installiation Instructions

* Build the project by executing 

```
$ mvn package
```

* Copy compiled plugin into Neo4j plugis folder

```
cp neo4j-auth/target/neo4j-auth-1.0.0.jar /path/to/neo4j/plugins/
```

* Edit neo4j configuration file. 

```
vi /path/to/neo4j/conf/neo4j-server.properties
```

* Add folowing line:

```
org.neo4j.server.thirdparty_jaxrs_classes=org.neo4j.extensions.server.unmanaged=/unmanaged
```

Plese pay attension for `extensions` word in the package name. Neo4j configuration file usually include sample line for such configration, but it will have different package name and server will not work.

 
* Start or restart neo4j 

## Ussage

* Adding new user:

curl --data "password={password}" --user neo4j:{neo4j.password} http://localhost:7474/unmanaged/auth/adduser/{user}

* Deleting user:

curl --user neo4j:{neo4j.password} http://localhost:7474/unmanaged/auth/delete/{user}
 
