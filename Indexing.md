# Index

An index is a special lookup table that helps speed up the process of retrieving data from a database.

An index helps to speed up the retrieval process like select query with a where class, but it slows down the input process, like Update, Insert

We can create and drop the index, it won't affect in data.


types of indexes but one of the most common types is the clustered index.  
- SQL Server can look at indexes quickly and easily instead of searching sequentially through potentially a large table.
- This is similar to the operating system to cache a lot of indexes into memory for faster access and for the file system to read a huge number of records simultaneously rather than reading them from the disk.

## Type of Indexing:
1)  Clustered Index


```
CREATE TABLE dbo.EmployeePhoto
(EmployeeId      INT NOT NULL PRIMARY KEY, 
 Photo           VARBINARY(MAX) NULL, 
 MyRowGuidColumn UNIQUEIDENTIFIER NOT NULL
                                  ROWGUIDCOL UNIQUE
                                             DEFAULT NEWID()
);
```

- You’ll notice in the create table definition for the “EmployeePhoto” table, that the primary key is at the end of the “EmployeeId” column definition. This creates an SQL index that is specially optimized to be used a lot.
- When the query is executed, **SQL Server will automatically create a clustered index** on the specified column.
- Notice that not only creating a **primary key creates a unique SQL index**
- a unique or primary key constraint should be created on the column when data integrity is the objective because by doing so the objective of the index will be clear.

2) primary Index
    
4) 
# Ref Link:
[https://www.simplilearn.com/tutorials/sql-tutorial/index-in-sql](https://www.simplilearn.com/tutorials/sql-tutorial/index-in-sql)
[https://www.sqlshack.com/sql-index-overview-and-strategy/](https://www.sqlshack.com/sql-index-overview-and-strategy/)
