##Examples of Cypher Queries:

### Find classes that group (i.e A) has on (i.e Monday)
MATCH (n:StudentGroup { group: 'A' })-[:on]->(b)-[]->(c) Where b.day = "Monday" RETURN n,b,c

### show all lecturers and what they are teaching
MATCH p=()-[r:has]->() RETURN p LIMIT 25

### Create Relationship Where Certain Lecturer has certain Class
b.kind can be changed to b.title

MATCH (a:Lecturer { name: 'Patrick Mannion' }), (b:Class { title: 'Database Mgmt' })
Where b.kind = "Lab"
CREATE (a)-[:has]->(b)


### Delete Where Certain Lecturer has a certain class
b.kind can be changed to b.title

MATCH (a:Lecturer)-[r:has]-(b:Class) 
Where a.name = "Patrick Mannion" and b.kind = "Lab"
DELETE r
