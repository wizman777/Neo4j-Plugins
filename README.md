## Installiation Instructions

1. Build the project by executing 

```
$ mvn package
```

2. Copy compiled plugin into Neo4j plugis folder

cp neo4j-auth/target/neo4j-auth-1.0.0.jar /path/to/neo4j/plugins/

3. Edit neo4j configuration file. 

vi /path/to/neo4j/conf/neo4j-server.properties

4. Add or uncomment folowing line:

org.neo4j.server.thirdparty_jaxrs_classes=org.neo4j.extensions.server.unmanaged=/unmanaged

(note double equals sing used in the property line)

5. Start or restart neo4j 

