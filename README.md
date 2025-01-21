This is a solution to the problem statement provided by Incubyte.

Problem Statement: 
Managing a global multi-specialty hospital chain requires an efficient system to handle billions of customer records daily. 
The data needs to be split into country-specific tables based on customer location, with mechanisms to track customers who visit from different countries. 
Additional requirements include deriving meaningful insights like age and days since last consultation, ensuring data integrity, and handling dynamic updates for shifting customers. 
The solution must scale effectively to process massive datasets while maintaining performance and accuracy.


Solution Approach:
Utilize a staging table and employ the COPY INTO command to efficiently load data from source files.
Create country-specific tables to organize and store data based on customer locations.
While populating country tables, calculate derived columns like age and days_since_last_consulted for additional insights.
Develop a procedure to execute a MERGE INTO command daily, ensuring seamless updates and insertions. If a record already exists in the target table, update its values; otherwise, insert it as a new record.
