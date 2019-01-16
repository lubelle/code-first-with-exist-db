## entity framework 6.2.0

code first with existing database
steps:

1. project
->add
->new item
->ADO.NET Entity Data Model
->Name="PlutoContext"
-> Code First from database
->New Connection
->Select the right database
->select all database objects except _MigrationHistory
->finish

2. PM>enable-migrations
3. PM>add-migration InitialModel
4. PM>add-migration InitialModel -IgnoreChanges -Force
5. PM>update-database
6. In SSMS, verify the database now has a dbo._MigrationHistory table
