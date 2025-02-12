<p><a target="_blank" href="https://app.eraser.io/workspace/AK1I4YQwEpQmVPGHNHQS" id="edit-in-eraser-github-link"><img alt="Edit in Eraser" src="https://firebasestorage.googleapis.com/v0/b/second-petal-295822.appspot.com/o/images%2Fgithub%2FOpen%20in%20Eraser.svg?alt=media&amp;token=968381c8-a7e7-472a-8ed6-4a6626da5501"></a></p>

>> Consider we are going to use our SQL in a website to upload videos for student, so we have to design database accordingly.

>> We can use Microsoft Visio, [﻿draw.io](https://draw.io/), lucid charts and more similar to this.

>> Represents the entities and their relationships like we can use ER (Entity Relationship) and UML. Both are similar but we will use mostly ER Diagram, and we will see going forwards.

>> Always when we say that we are designing database then we should make sure you have to follow these below steps to achieve it:



## Conceptual Model
>> It just like sample diagram to understand the flow of data and tables goes in `SQL;` to further check with team and stake holder's but it `doesn't` give many details about the design.



## Logical Model
>> It is just extra layer on top of conceptual model and if you see the below diagram, it gives us more information about the relationships and entities datatypes to be used.

Note: The String, Fload & DataTimes is not actual supported datatypes but just to give proper picture we will use this, but we will used the actual datatypes as the database you are using like MySQL, SQL Server, Oracle, MongoDB, etc.


### In SQL we have 4 types of relationships which follows below:
1. One-to-one
2. One-to-many
3. Many-to-one
4. Many-to-many




## Physical Model
-- We have to create new physical model, to do in MySQL Workbench click on File >> New Model.
-- By default, the my dB model will be present and if you want you can change it.
-- At the top you can see new EE Diagram, double-click on that to get to create the physical model.







## Primary Keys
-- It is unique to identify the table data so that there should not be any duplicate.





## Foreign Keys & Composite Key
-- It is referred from the parent primary key column.
-- When we specify two different table primary key referring the child table then we can set those 2 primary keys as primary key for the child table, and this is called composite key.






## Foreign Keys Constraints
-- When we use Foreign Keys in child table and suppose if you delete some data in the main table so what this foreign key table data should do.
-- We can set these values to CASCADE, so whenever there is update in primary table with respect to primary key, it should automatically delete.

-- Most of the time we set it to CASCADE on update and RESTRICT/NOACTION for delete, but it depends on use case as well.






## -------------// Normalization //----------------
-- Is process of reviewing the design and ensuring that it follows a few pre-defined roles which prevent us from data duplication.
-- We have 7 of them and each rule assumes that you have applied the previous rules.
-- 99% of the application we have to apply only this 3 NF, and we really do not need to worry about the other NF.





## 1 NF
-- Each cell in a row should have Single value and we cannot have repeated columns.

-- If we look at `tag's` column in the table, we will find out that we can so many tags in a table or we have separated the tags by comma, so we can remove the tags column to new separate table and create relations between them many-to-many.





## Link Tables
-- In relation database we** don't have many-to-many relationships**, to achieve this we have to create one newer table and then create 2 one-to-many relationship to make it work.

**Note: Doing this now our table is in 1 NF, means we don't have any duplicates.**





## 2 NF
-- Each T**able** should have **one entity**, and every column in that table should describe that entity.

-- Now if you have look at the Courses table, we have one different entity, and it should not be there so we will create new table with name instructor.

Example: We have already discussed this, if you look at the diagram the Enrollment table it was derived from the Course Table as it was not marching with the course table.







## 3 NF
-- In simple words "**a column in a table should not be derived from other columns**"

-- 3NF takes it further by **removing transitive dependencies, a situation where non-key attributes depend indirectly on the primary key**. 

By focusing on this, 3NF ensures that each non-key column in a table is directly tied to the primary key and nothing else.

**Example 1**: You can see that we can get the balance details by subtracting the invoice total and payment total, but the balance amount will remain same if we change invoice total or payments total in future, so we have to remove balance column from here and put this in different table.



**Example 2**: We can see that we have first, last and full name column name in a table, which is violating the 3NF because we can always get full name by combining first and last name. 







## Forward Engineering a Model
-- So far, we have just created ER model or Physical model, to move forward with the database will create the actual database by clicking on database menu from the top and then click on forward engineer to database.





## Synchronizing a Model with a Database
-- Now we have problem when we later update the ER model, and we want to make sure the changes took place overall place and network so we will do synchronizing option once making the changes. We added coupon column in our table enrollment, and we will do sync to database option.





## Reverse Engineering a Model
-- Suppose if you don't have database model for particular database then we can create using reverse engineering and make the changes required.

![image.png](/.eraser/AK1I4YQwEpQmVPGHNHQS___7JEavVdR9CMTh9Mw4v2EFMgjxqo1___4chMZtprrM0GVbUnMBCnA.png "image.png")







## Create Model on Flight Booking System
![Screenshot 2025-02-12 at 06.07.22.png](/.eraser/AK1I4YQwEpQmVPGHNHQS___7JEavVdR9CMTh9Mw4v2EFMgjxqo1___hnrhLMXi9IvT7rT7CQhzn.png "Screenshot 2025-02-12 at 06.07.22.png")









## Project - Video Rental Application
![Screenshot 2025-02-12 at 06.09.15.png](/.eraser/AK1I4YQwEpQmVPGHNHQS___7JEavVdR9CMTh9Mw4v2EFMgjxqo1___s38PNopCOf6JJYlgjgVpt.png "Screenshot 2025-02-12 at 06.09.15.png")




<!-- eraser-additional-content -->
## Diagrams
<!-- eraser-additional-files -->
<a href="/MySQL/DB_Design_ER-entity-relationship-1.eraserdiagram" data-element-id="LiosVctDX7whzvDjuRBcv"><img src="/.eraser/AK1I4YQwEpQmVPGHNHQS___7JEavVdR9CMTh9Mw4v2EFMgjxqo1___---diagram----ff89dce6eae396a8df6c2c672fc931e2.png" alt="" data-element-id="LiosVctDX7whzvDjuRBcv" /></a>
<a href="/MySQL/DB_Design_ER-entity-relationship-2.eraserdiagram" data-element-id="XPqF3RIZtmAazXGr8k1j3"><img src="/.eraser/AK1I4YQwEpQmVPGHNHQS___7JEavVdR9CMTh9Mw4v2EFMgjxqo1___---diagram----aceb0acfb9d2d30fec2a9f60770a5b12.png" alt="" data-element-id="XPqF3RIZtmAazXGr8k1j3" /></a>
<!-- end-eraser-additional-files -->
<!-- end-eraser-additional-content -->
<!--- Eraser file: https://app.eraser.io/workspace/AK1I4YQwEpQmVPGHNHQS --->