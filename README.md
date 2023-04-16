# Football Tournament

N.B. for more information and examples, please see the attached project presentation in the SQL repository

## Brief: 

The company was running a football tournament that consisted of 6 players aside, four teams and 8 groups participating. 3 points for a win, 1 for a draw and 0 for a loss. My task (whilst working alongside a colleague) was to create a relational database that stores all data retrieved from goals scored to whoever got a red card.

## ER Design: 
1st experience of drafting an entity relationship diagram. This would summarise structured data through many-to-one and one-to-many connections.


![ER design for football tournament](https://user-images.githubusercontent.com/116355407/232313034-7a1c1f8b-970f-40ff-b2c6-f92e89930421.png)
This is a diagram of normalising a database. This helps improve the speed, accuracy and efficiency of the database when executing queries. This was organised via:

-Conceptual Schema (The general database structure): Cards, Goals, Results, Matches etc.
-Logical Schema (Objects within the conceptual schema that is defined by information): Club ID, Home Club, Player Name, Venue Name etc.
-Physical Schema (How data is represented and stored): ID's should be stored as integers and names of someone or something should be strings.

## Implementation: 
Using Postgresql, for our DDL (Data Definition Language), we used the graphical user interface on pg admin 4 to assist in devising the conceptual and logical schema.
All were further populated via DML (Data Manipulation Language) manually using SQL code

Defining table schemas using Graphical User Interface:

![Creating a table using pgadmin GUI](https://user-images.githubusercontent.com/116355407/232313815-95af2f33-2e48-4d92-bdc2-ee2b3af047fd.png)

Using Data Manipulation Language to populate schemas (file name was changed for data protection):

![Data Manipulation Language edt](https://user-images.githubusercontent.com/116355407/232314977-6b87e620-25cf-45da-8a43-c2fc5de27268.png)

## Some Queries to answer data related questions:
General representation of SQL prowess in practice. These are a representation of simple SQL queries to more advanced SQL queries. More information can be found in the attached powerpoint

### 4) Return the number of goals scored in the season 

<img width="417" alt="Question 4 query" src="https://user-images.githubusercontent.com/116355407/232316369-1eba1949-7e9a-4326-b1f7-08fc23c70e43.png">
<img width="309" alt="Question 4 query output" src="https://user-images.githubusercontent.com/116355407/232316373-e3ba0588-00de-422c-b8ed-44a292842dea.png">

### 5) Return the number of goals in favour, goals against, goals difference and points by team

<img width="452" alt="question 5 query" src="https://user-images.githubusercontent.com/116355407/232316620-c4fc737a-ac8d-4314-a887-087074a8002a.png">
<img width="452" alt="question 5 query output" src="https://user-images.githubusercontent.com/116355407/232316629-91555bc1-ed4f-4755-bdf3-7d1b0f6ccbdb.png">

### 8) Develop a store procedure to add new players. It needs to consider warnings and exceptions 

<img width="452" alt="question 8 query" src="https://user-images.githubusercontent.com/116355407/232317026-2911c72a-22b3-4edf-b296-8797503b539b.png">

## Conclusions:
The Vis Wizards delivered a very strong performance. Alvin Ali and Jamya Dodson were the leading goal scorers. The Data Cleaners had the weakest performance and were 1/2 teams that had a negative goal difference. The Data Cleaners also need to monitor player behaviour and conduct as they accumulated the most red cards all season

## Reflections:
This was the first experience of ER design. This process takes time but an essential one when a relational database is created. If one person is assigned to the task it can take days but with multiple people, it can be completed within the day.

As SQL knowledge has grown, question no. 5 can be tidyer, making it more efficient and consume less memory. The query has lots of sub queries and this can be replaced with 1 (at most 2) common table expressions.

Finally, this was the first experience of designing relational databases in SQL and the basics of ETL/ELT strategies. The simplest approach is always the best approach so if this would be attempted again, the GUI will be used to create the schemas and the same DML construct will be used to populate. If repeating these queries, the questions that devised an output with lots of sub queries will be replaced with CTE's





