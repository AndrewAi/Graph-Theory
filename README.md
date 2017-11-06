# Graph-Theory

## Project Brief

The following document contains the instructions for Project 2017 for Graph Theory. You are required to design and prototype a Neo4j database for use in a timetabling system for a third level institute like GMIT. 
The database should store information about student groups, classrooms, lecturers, and work hours – just like the currently used timetabling system at GMIT.

## What Data needs to be stored
- Student Groups
- Classrooms
- Lecturers
- Work Hours
- Classes
____
## How Data is represented in the Database

This part of the project is probably the hardest and most challenging because it requires a huge amount of thought
and also there is no real correct answer, as the data can always be represented in a different way which may be precieved better.

Initially I found this project difficult, I really enjoyed how much it allowed me to be creative! I also like the fact that I all needed was to be creative and to think and really draw it out, and not needing so much of a technical knowledge in order to do well.
I also found the Neo4j Cypher Queries/Language to be quite in intutive and easy to learn. 
I had a fairly good grasp of the language after 2 days and found it was so intutive that I could actually make up & guess queries and they would be actually right, as once you learn the basics you can adapt and manipulate them. 

I started out by writing out on paper what are the key values that needed to be represented :
- Student Groups
- Classrooms
- Lecturers
- Work Hours
- Classes

I then drew rough models of what I thought the system/ database might look like.

![alt tag](https://github.com/AndrewAi/Graph-Theory/blob/master/DbDesign1%2023.14.15.png)


Once I had drawn a rough design and felt it had good logic, I went onto create a test prototype on Neo4j of all nodes (classes,lectures,times,days,rooms etc) on one day (i.e Monday) to see what it would actually look like and react & co-operate before trying to add in all the data and potenially have a big huge mess. 
I found that are after fleshing the design with test data, flaws & cracks quickly started to appear, So I had to go back to the drawing board,
but this time I knew where the faults lied so I was able to design around them.

![alt tag](https://github.com/AndrewAi/Graph-Theory/blob/master/DbDesign2%2023.14.15.JPG)

This time I draw out a more extensive drawing which included all 3 groups over 2 days, on when & where they had a particular class (i.e Software Testing) I could see this design straight away appeared to be more scalable. 
I even added in a different class to see how it all would fair out.

Once happy, I went onto neo4j again, and began to carefully build up the database. Once I could see everything was going ok.
I designed a template query which allowed me to create a full relationship from StudentGroup -on-> Monday -atTime-> -inRoom-> Software Testing. Designing this robust and long query helped alot and saved alot of time, as I had spent a lot of time trying to figure out how to automattically import all the data into neo4j in one fell swoop! but eventually ran out of time and had to import otherwise so I made custom query:

![alt tag](https://github.com/AndrewAi/Graph-Theory/blob/master/Create%20Query.png)

That Was very useful.

I ended up with a design that looked like this.
## Final Design Representation:

![alt tag](https://github.com/AndrewAi/Graph-Theory/blob/master/GroupAClasses.png)

This design meant there was no duplication of nodes and that you could easily see what node had a relationship with another.


_____
## Installation:
- Download & Install Neo4j (if you do not have it already)
- Clone or Download this repo
- Open Neo4j, find and select the location of default.graphdb
  Smile
  
## References:
Neo4j - Delete a Relationship using Cypher
http://www.quackit.com/neo4j/tutorial/neo4j_delete_a_relationship_using_cypher.cfm

Neo4j- Set Clause

http://neo4j.com/docs/snapshot/query-set.html

Neo4j- Set Clause

http://neo4j.com/docs/developer-manual/current/cypher/clauses/remove/

StackOverflow - how to add a property to existing node neo4j cypher?

http://stackoverflow.com/questions/24407716/how-to-add-a-property-to-existing-node-neo4j-cypher

Add images to README.md on GitHub

http://stackoverflow.com/questions/14494747/add-images-to-readme-md-on-github
