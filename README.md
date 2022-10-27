# Data Lineage for Microsoft T-SQL Queries 

Data Lineage Transact SQL (T-SQL) for [Microsoft SQL Server](https://www.microsoft.com/en-us/sql-server) or [Azure SQL Server](https://azure.microsoft.com/en-us/services/sql-database/campaign/) enables you to find the data origins and data destinations in your query. It gives you the visibility over query data columns and ability to track the changes over time.


# Features

* Remove any kind of comments from your T-SQL code
* Remove any special characters from your T-SQL code
* Generate data lineage from your T-SQL Code
* Learn interesting facts about your data and get better analytics



# Removing comments from your T-SQL code
Clean your code of in-line and multiple lines of _--comments_ or _slash star_ comments from better visibility and greater readability.

<a href="https://tomaztsql.files.wordpress.com/2021/07/2021-07-13-05_24_06-window.png"><img width="50%" src="https://tomaztsql.files.wordpress.com/2021/07/2021-07-13-05_24_06-window.png"/>
</a>
  
Run **Remove_comments.sql**  to create  a procedure. 
Strip and remove all comments from your T-SQL query by using _dbo.remove_comments_ procedure 

``` sql
--  Run procedure dbo.remove_comments

EXEC dbo.remove_comments
   @procedure_name = N'dbo.MySample_procedure'

```


# Start with Data Lineage on T-SQL

Run **TSQL_data_lineage.sql**  file to create  a lineage procedure. This script includes the removal of comments and special characters and creates the data lineage.


```sql
-- Get your query:
DECLARE @test_query VARCHAR(MAX) = '

-- This is a sample query to test data lineage
SELECT 
    s.[BusinessEntityID]
    ,p.[Title]
    ,p.[FirstName]
    ,p.[MiddleName]
   -- ,p.[LastName]
    ,p.[Suffix]
    ,e.[JobTitle] as JobName
    ,p.[EmailPromotion]
    ,s.[SalesQuota]
    ,s.[SalesYTD]
    ,s.[SalesLastYear]
	,( SELECT GETDATE() ) AS DateNow
	,( select count(*)  FROM [AdventureWorks2014].sales.[SalesPerson] ) as totalSales

/*

Adding some comments!

*/

FROM [AdventureWorks2014].sales.[SalesPerson] s
    LEFT JOIN [AdventureWorks2014].[HumanResources].[Employee] e 
    ON e.[BusinessEntityID] = s.[BusinessEntityID]
	INNER JOIN [AdventureWorks2014].[Person].[Person] AS p
	ON p.[BusinessEntityID] = s.[BusinessEntityID]

'

-- And run the procedure with single input parameter
EXEC dbo.TSQL_data_lineage 
  @InputQuery = @test_query
```

# Requirements

The script works with any of the following versions:

* Microsoft SQL Server database (works on all editions and versions 2016+) 
* Azure SQL Database 
* Azure SQL Server 
* Azure SQL MI 



Get started
===========
The easiest way to get started is with fork or clone the repository.


## Cloning the repository
You can follow the steps below to clone the repository.
```
git clone https://github.com/tomaztk/SQLServer-Data-Lineage.git
```

## Read more on blog posts

Remove comments from your T-SQL code ([Blog post](https://tomaztsql.wordpress.com/2021/07/13/remove-comments-from-your-t-sql-code/))


## Collaboration and contributors
Ideas, code collaboration or any other contributions of any kind is highly appreciated! 
Fork the repository, add your code.

# Data Lineage for Microsoft T-SQL Queries 

Data Lineage Transact SQL (T-SQL) for [Microsoft SQL Server](https://www.microsoft.com/en-us/sql-server) or [Azure SQL Server](https://azure.microsoft.com/en-us/services/sql-database/campaign/) enables you to find the data origins and data destinations in your query. It gives you the visibility over query data columns and ability to track the changes over time.


# Features

* Remove any kind of comments from your T-SQL code
* Remove any special characters from your T-SQL code
* Generate data lineage from your T-SQL Code
* Learn interesting facts about your data and get better analytics



# Removing comments from your T-SQL code
Clean your code of in-line and multiple lines of _--comments_ or _slash star_ comments from better visibility and greater readability.

<a href="https://tomaztsql.files.wordpress.com/2021/07/2021-07-13-05_24_06-window.png"><img width="50%" src="https://tomaztsql.files.wordpress.com/2021/07/2021-07-13-05_24_06-window.png"/>
</a>
  
Run **Remove_comments.sql**  to create  a procedure. 
Strip and remove all comments from your T-SQL query by using _dbo.remove_comments_ procedure 

``` sql
--  Run procedure dbo.remove_comments

EXEC dbo.remove_comments
   @procedure_name = N'dbo.MySample_procedure'

```


# Start with Data Lineage on T-SQL

Run **TSQL_data_lineage.sql**  file to create  a lineage procedure. This script includes the removal of comments and special characters and creates the data lineage.


```sql
-- Get your query:
DECLARE @test_query VARCHAR(MAX) = '

-- This is a sample query to test data lineage
SELECT 
    s.[BusinessEntityID]
    ,p.[Title]
    ,p.[FirstName]
    ,p.[MiddleName]
   -- ,p.[LastName]
    ,p.[Suffix]
    ,e.[JobTitle] as JobName
    ,p.[EmailPromotion]
    ,s.[SalesQuota]
    ,s.[SalesYTD]
    ,s.[SalesLastYear]
	,( SELECT GETDATE() ) AS DateNow
	,( select count(*)  FROM [AdventureWorks2014].sales.[SalesPerson] ) as totalSales

/*

Adding some comments!

*/

FROM [AdventureWorks2014].sales.[SalesPerson] s
    LEFT JOIN [AdventureWorks2014].[HumanResources].[Employee] e 
    ON e.[BusinessEntityID] = s.[BusinessEntityID]
	INNER JOIN [AdventureWorks2014].[Person].[Person] AS p
	ON p.[BusinessEntityID] = s.[BusinessEntityID]

'

-- And run the procedure with single input parameter
EXEC dbo.TSQL_data_lineage 
  @InputQuery = @test_query
```

# Requirements

The script works with any of the following versions:

* Microsoft SQL Server database (works on all editions and versions 2016+) 
* Azure SQL Database 
* Azure SQL Server 
* Azure SQL MI 



Get started
===========
The easiest way to get started is with fork or clone the repository.


## Cloning the repository
You can follow the steps below to clone the repository.
```
git clone https://github.com/tomaztk/SQLServer-Data-Lineage.git
```

## Read more on blog posts

Remove comments from your T-SQL code ([Blog post](https://tomaztsql.wordpress.com/2021/07/13/remove-comments-from-your-t-sql-code/))


## Collaboration and contributors
Ideas, code collaboration or any other contributions of any kind is highly appreciated! 
Fork the repository, add your code.

# Data Lineage for Microsoft T-SQL Queries 

Data Lineage Transact SQL (T-SQL) for [Microsoft SQL Server](https://www.microsoft.com/en-us/sql-server) or [Azure SQL Server](https://azure.microsoft.com/en-us/services/sql-database/campaign/) enables you to find the data origins and data destinations in your query. It gives you the visibility over query data columns and ability to track the changes over time.


# Features

* Remove any kind of comments from your T-SQL code
* Remove any special characters from your T-SQL code
* Generate data lineage from your T-SQL Code
* Learn interesting facts about your data and get better analytics



# Removing comments from your T-SQL code
Clean your code of in-line and multiple lines of _--comments_ or _slash star_ comments from better visibility and greater readability.

<a href="https://tomaztsql.files.wordpress.com/2021/07/2021-07-13-05_24_06-window.png"><img width="50%" src="https://tomaztsql.files.wordpress.com/2021/07/2021-07-13-05_24_06-window.png"/>
</a>
  
Run **Remove_comments.sql**  to create  a procedure. 
Strip and remove all comments from your T-SQL query by using _dbo.remove_comments_ procedure 

``` sql
--  Run procedure dbo.remove_comments

EXEC dbo.remove_comments
   @procedure_name = N'dbo.MySample_procedure'

```


# Start with Data Lineage on T-SQL

Run **TSQL_data_lineage.sql**  file to create  a lineage procedure. This script includes the removal of comments and special characters and creates the data lineage.


```sql
-- Get your query:
DECLARE @test_query VARCHAR(MAX) = '

-- This is a sample query to test data lineage
SELECT 
    s.[BusinessEntityID]
    ,p.[Title]
    ,p.[FirstName]
    ,p.[MiddleName]
   -- ,p.[LastName]
    ,p.[Suffix]
    ,e.[JobTitle] as JobName
    ,p.[EmailPromotion]
    ,s.[SalesQuota]
    ,s.[SalesYTD]
    ,s.[SalesLastYear]
	,( SELECT GETDATE() ) AS DateNow
	,( select count(*)  FROM [AdventureWorks2014].sales.[SalesPerson] ) as totalSales

/*

Adding some comments!

*/

FROM [AdventureWorks2014].sales.[SalesPerson] s
    LEFT JOIN [AdventureWorks2014].[HumanResources].[Employee] e 
    ON e.[BusinessEntityID] = s.[BusinessEntityID]
	INNER JOIN [AdventureWorks2014].[Person].[Person] AS p
	ON p.[BusinessEntityID] = s.[BusinessEntityID]

'

-- And run the procedure with single input parameter
EXEC dbo.TSQL_data_lineage 
  @InputQuery = @test_query
```

# Requirements

The script works with any of the following versions:

* Microsoft SQL Server database (works on all editions and versions 2016+) 
* Azure SQL Database 
* Azure SQL Server 
* Azure SQL MI 



Get started
===========
The easiest way to get started is with fork or clone the repository.


## Cloning the repository
You can follow the steps below to clone the repository.
```
git clone https://github.com/tomaztk/SQLServer-Data-Lineage.git
```

## Read more on blog posts

Remove comments from your T-SQL code ([Blog post](https://tomaztsql.wordpress.com/2021/07/13/remove-comments-from-your-t-sql-code/))


## Collaboration and contributors
Ideas, code collaboration or any other contributions of any kind is highly appreciated! 
Fork the repository, add your code.



# Create dependency table of code even if embedded in strings.

```sql
IF OBJECT_ID('dbo.tblObjDeps') is not null drop table dbo.tblObjDeps;

create table dbo.tblObjDeps (parentObjectId INT NOT NULL, childObjectId INT NOT NULL, CONSTRAINT pk_tblObjDeps PRIMARY KEY CLUSTERED (parentObjectId, childObjectId));

with
no_comment_blocks as
(
   select object_id, string_agg(iif(e > 0, substring(txt, e+2, len(txt)), txt),'') txt
   from (select object_id, CHARINDEX('*/', value) e, value as txt
         from sys.objects
         cross apply string_split(REPLACE(OBJECT_DEFINITION(object_id),'/*',char(1)),char(1), 1)
         where type in ('FN','P','TF','V')) a
   group by object_id
)
,no_comment_lines as
(
   select object_id, string_agg(iif(e > 0, substring(txt, e, len(txt)), txt),'') txt
   from (select object_id, CHARINDEX(char(13)+char(10), value) e, value as txt
         from no_comment_blocks
         cross apply string_split(REPLACE(txt,'--',char(1)),char(1), 1)) a
   group by object_id
)
insert into dbo.tblObjDeps (parentObjectId, childObjectId)
select distinct
       iif(relType = 'PARENT', relObjectId, objectId) as parentObjectId
      ,iif(relType = 'CHILD' , relObjectId, objectId) as childObjectId
from (select objectId, relObjectId, relType, row_number() over (partition by objectId, relObjectid order by relType) as ord
      from (select distinct
                   objectId
                  ,relObjectId
                  ,iif(preText like '% DELETE FROM' or preText like '% TRUNCATE TABLE', 'PREP'
                      ,iif(preText like '% JOIN' or preText like '% FROM' or preText like '% EXEC' or preText like '% (', 'PARENT'
                          ,iif(preText like '% MERGE' or preText like '% INTO' or preText like '% UPDATE' or preText like '% TABLE' or preText like '% VIEW', 'CHILD'
                              ,'SKIP'))) as relType
            from (select objectId
                        ,rtrim(left(prev,greatest(len(prev)-len(relSchemaName)-1,0))) as preText
                        ,object_id(relSchemaName+'.'+relObjectName) as relObjectId
                  from (select objectId
                              ,prev
                              ,right(prev, greatest(charindex(' ', reverse(prev))-1,0)) as relSchemaName
                              ,relObjectName
                        from (select objectId
                                    ,lag(val, 1, null) over (partition by objectId order by row) as prev
                                    ,left(val, greatest(charindex(' ', val)-1,0)) as relObjectName
                              from (select object_id as objectId, ordinal as row, value as val
                                    from   no_comment_lines
                                    cross apply string_split(REPLACE(REPLACE(REPLACE(txt,char(9),' '),char(13)+char(10),' '),'(',' ( '),'.', 1)
                                   ) a
                             ) b
                       ) c
                 ) d
            where relObjectId > 0 and relObjectId != objectId
           ) e
      where relType in ('CHILD','PARENT')
     ) f
where ord = 1;
```

## Query child dependencies


```sql
with
generation AS (
    SELECT parentObjectId
                    ,childObjectId
                            ,cast(OBJECT_SCHEMA_NAME(childObjectId) as varchar(max))+'.'+cast(OBJECT_NAME(childObjectId) as varchar(max)) + ' <- '+cast(OBJECT_SCHEMA_NAME(parentObjectId) as varchar(max))+'.'+cast(OBJECT_NAME(parentObjectId) as varchar(max)) AS descendants
    FROM dbo.tblObjDeps
    WHERE parentObjectId = object_id(@objectName)
    UNION ALL
    SELECT d.parentObjectId
                    ,d.childObjectId
                            ,cast(OBJECT_SCHEMA_NAME(d.childObjectId) as varchar(max))+'.'+cast(OBJECT_NAME(d.childObjectId) as varchar(max)) +' <- '+descendants AS descendants
    FROM dbo.tblObjDeps d
              JOIN generation g ON g.childObjectId = d.parentObjectId
)
SELECT descendants as [CHILD <- PARENT]
FROM generation
order by descendants
OPTION (MAXRECURSION 10000);
```

## Query parent dependencies


```sql
with
generation AS (
    SELECT parentObjectId
                    ,childObjectId
                              ,cast(OBJECT_SCHEMA_NAME(parentObjectId) as varchar(max))+'.'+cast(OBJECT_NAME(parentObjectId) as varchar(max)) + ' <- '+cast(OBJECT_SCHEMA_NAME(childObjectId) as varchar(max))+'.'+cast(OBJECT_NAME(childObjectId) as varchar(max)) AS parentage
    FROM dbo.tblObjDeps
    WHERE childObjectId = object_id(@objectName)
    UNION ALL
    SELECT d.parentObjectId
                    ,d.childObjectId
                              ,cast(OBJECT_SCHEMA_NAME(d.parentObjectId) as varchar(max))+'.'+cast(OBJECT_NAME(d.parentObjectId) as varchar(max)) +' <- '+parentage AS parentage
    FROM dbo.tblObjDeps d
              JOIN generation g ON g.parentObjectId = d.childObjectId
)
SELECT parentage as [PARENT <- CHILD]
FROM generation
OPTION (MAXRECURSION 10000);
```
