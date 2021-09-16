SQL session:

IN - Returns true if a value matches any value in the list BETWEEN - Return true if a value is between a range of values ex. BETWEEN 3 AND 5 LIKE - Return true if a value matches a pattern ex. LIKE 'Aud%' means match string starting with 'Aud'. ILIKE - Same as LIKE but case insensitive pattern matching. OFFSET - Skip a number of rows before returning the resultset LIMIT - To constrain the number of rows returned by a query (not a SQl standard) FETCH - Same as LIMIT and it a SQL standard. Syntax -> FETCH {FIRST|NEXT} row_cnt {ROW|ROWS} ONLY LEFT(s, n) - Extracts first n characters from s ALL - We can use the word ALL to allow >= or > or < or <= to act over a list ex. on result of select subquery

ORDER BY - Sort thr column in ASC or DESC order GROUP BY - Functions such as SUM and COUNT are applied to groups of items sharing values.ex."GROUP BY continent" ,the result is only one row for each different value of continent. All the other columns must be "aggregated" by one of SUM, COUNT etc. WHERE - filters the rows before aggregation operation HAVING - filters after the agregation

Some important psql commands:

sudo -u psql --> switched to and starts psql command prompt

\c dbname username --> switch connection to new database (dbname) under a user specified by

\l --> list all available databases

\dt --> list all tables in current database

\d table_name --> describe a table

\dn --> list all Schemas of current database

\df --> list all functions of current database

\dv --> list all Views of current database

\du --> list all users and their assigned roles

\s --> to display command history

\g --> to execute previous command

\i filename --> to execute psql commands from a file

\timing --> to turn ON/OFF query execution time:w

\e --> to write command in default editor(vim/nano)

\q --> to quit psql

COMMON QUERIES:

Create new user --> CREATE USER username WITH PASSWORD 'password';
Drop user --> DROP USER IF EXISTS username;
Create new database --> CREATE DATABASE db_name;
Grant privileges --> GRANT ALL|SELECT|UPDATE|DELETE PRIVILEGES ON DATABASE db_name TO username;
Drop database --> DROP DATABASE IF EXISTS db_name;
Create schema --> CREATE SCHEMA schema_name [CASCADE];
Create table --> CREATE TABLE tb_name
Insert data --> INSERT INTO tb_name(col1, col2,...) VALUES (val1, val2,...);
Update Column --> UPDATE tb_name SET col = val WHERE condition;
Delete row --> DELETE FROM tb_name WHERE condition;
Delete table --> DROP TABLE IF EXISTS tb_name;
Evaluation order in Queries:

FROM --> WHERE --> SELECT --> ORDER BY

For creating users and db: https://www.youtube.com/watch?v=RySuQtMiBxQ
