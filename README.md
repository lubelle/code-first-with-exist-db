## entity framework 6.2.0

code first with existing database

## project
	add->new item->ADO.NET Entity Data Model->Name="PlutoContext"-> Code First from database->New Connection->Select the right database->select all database objects except _MigrationHistory->finish
	PM>enable-migrations PM>add-migration InitialModel PM>add-migration InitialModel -IgnoreChanges -Force PM>update-database In SSMS, verify the database now has a dbo._MigrationHistory table
## add new class
	add DbSet<newClass> in PlutoContext.cs PM>add-migration addNewClass add Sql() to addNewClass PM>update-database        







