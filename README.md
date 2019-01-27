## Entity framework 6.2.0

code first with existing database

## Project
	add->new item->ADO.NET Entity Data Model->Name="PlutoContext"-> Code First from database->New Connection->Select the right database->select all database objects except _MigrationHistory->finish
	PM>enable-migrations PM>add-migration InitialModel PM>add-migration InitialModel -IgnoreChanges -Force PM>update-database In SSMS, verify the database now has a dbo._MigrationHistory table
## Working with classes
	-adding a new class: add DbSet<newClass> in PlutoContext.cs PM>add-migration addNewClass add Sql() to addNewClass PM>update-database
	-adding a new property
	-modifying an existing property
	-deleting an existing proerty
## Downgrading database
	-using a blank database:checkout the older version;change the db name in the connection string; update-database
	-using an existing database
	use latest source code; update-database -TargetMigration:<<name>>;checkout the right version of source code; checkout the latest version; update-database
## Seeding database
	





