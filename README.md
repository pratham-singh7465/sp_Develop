# sp_Develop
To check the health status of ms-sql tables
1. Download a copy of the stored procedure sp_Develop. Execute the stored procedure to create it on your SQL Server. 
2. After installing , EXECUTE dbo.sp_Develop;
3. To skip Checks , EXEC dbo.sp_Develop
   ,@SkipCheckDatabase = N'pubs'
   ,@SkipCheckSchema = N'dbo'
   ,@SkipCheckTable = N'DevelopCheckToSkip';
4. 
ColumnName  	                Details
Priority                    	Critical, High, Medium, Low
DatabaseName	                Can be run for multiple databases so this will show you the database with the potential issue
SchemaName	                  This is the schema for the object that might have an issue
ObjectName	                  This can be anything from user tables, views stored procedures, functions, …
FindingGroup                	The high-level grouping for the check
- Naming Conventions
- Table Conventions
- Data Type Conventions
- SQL Code Development
- Data Issue
- Configuration Issue
- Running Issues
Finding	                      The specific potential issue we the check is looking for
Details                     	Additional details about the potential issue. This does not go into in-depth details of the potential issue but should give you a heads up of what to look for
SkipCheckTSQL               	In this column you will find a generated TSQL script INSERT
PriorityNumber	              The lower the number the more severe the potential issue is to address
CheckId                      	Every check is uniquely numbered
