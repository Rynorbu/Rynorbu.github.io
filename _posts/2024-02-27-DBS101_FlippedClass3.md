---
Title: DBS101 Flipped Class3
categories: [DBS101, Flipped_class3]
tags: [DBS101]
---
## Topic: Null values and Set operations in SQL
---

Hello! Today, I want to share with you my experience and the knowledge I gained from my flipped class 3. Today's class was great, I learned and understood the basics of null values and set operations in SQL and their syntax representaion in SQL.

During our flipped class we are divided into two types of groups, home groups and expert groups, with six people in each. My job was to study set operations in SQL and share examples with our expert groups. Meanwhile, other groups focused on studying null values in SQL. It took me about 50 minutes to study set operations, and once I understood the concept, I explained it to my home group. They, in turn, shared their learnings from the 50-minute session on null values, and the whole explanation process took around 30 minutes. It was a wonderfull experience where we shared our knowldegeand and helped each other.

#### Set Operation
SQL is a tool used for handling databases. It helps organize and communicate with databases. In SQL, there are set operations that combine and compare different statements. These operations include Union, Union all, Intersect, and Minus. They are useful for working with and comparing data in a database.

#### 1. Union
The union sql set operation is used to combine two sets of rows and remove duplicates. We use the command 'UNION' to represent Union operation in SQL. 

UNION syntax
```
SELECT column_name FROM table1
UNION
SELECT column_name FROM table2;
```
#### 2. Union all
Union all set operation is used to Combine two sets of rows but without removing duplicates unlike union. We use 'UNION ALL' command to represent union all operation in SQL.

UNION ALL syntax
```
SELECT column_name FROM table1
UNION ALL  
SELECT column_name FROM table2;
```

#### 3. Intersect
This set operation is used to Find common rows between two sets. We use 'INTERSECT' command to represent insert operation in SQL.

INTERSECT syntax
```
SELECT column_name FROM table1  
INTERSECT  
SELECT column_name FROM table2;  
```

#### 4. Minus
This minus set operation gives you the rows that are in the first set but not in the second set. We have to use 'MINUS' command to represent minus operation in SQL.

MINUS syntax
```
SELECT column_name FROM table1  
MINUS  
SELECT column_name FROM table2;  
```

#### Null value  

A null value in SQL means something doesn't have any value. When dealing with records in a database, some data might be missing or unknown, and in SQL, we use the term "null" to represent this absence of value in a column. It's different from having a zero or an empty space – it specifically indicates that the data for that column is either unknown or undefined.

To check whether the attribute value is NULL or not, we have to use IS and IS NOT rather than using = to compare an attribute value in SQL.

IS NULL Syntax

```
SELECT column_names
FROM table_name
WHERE column_name IS NULL;
```

IS NOT NULL Syntax
```
SELECT column_names
FROM table_name
WHERE column_name IS NOT NULL;
```

