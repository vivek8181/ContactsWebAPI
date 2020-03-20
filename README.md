# ContactsWebAPI
Web API Demo
Introduction:
This is simple demo example of CRUD operations using ASP.NET REST API. 
This project uses the example of Contacts management, where you can list all contacts, add, edit, and delete or deactivate.

Technical Concepts used:
1. The Project uses backend as SQL Server database and uses EF with database first approach.
2. There is DataAccess layer implemented in Contacts.Infrastructure project.
3. Repository Pattern is used for accessing the database from API. 
4. Repository Pattern makes the service loosly coupled from database. Change in datastorage strategy will not affect the integrity of service. And easy to unit test.
5. Dependency injection is used to resolve the reference of Contacts repository. It Uses Unity.


Folder Structure:
1. Contacts.Infrastructure -- This is DataAccess layer
2. ContactsAPI -- This is implementation of API

How To Use project:
1. Project uses the SQL Database as backend storage, Run the "script.sql" to create the database.
2. Add Connection string in "ContactsWebAPI\ContactsAPI\Web.config" with Name "ContactsDBEntities2". 
e.g.
<add name="ContactsDBEntities2" connectionString="metadata=res://*/Contacts.csdl|res://*/Contacts.ssdl|res://*/Contacts.msl;provider=System.Data.SqlClient;provider connection string=&quot;data source=<SourceName>;initial catalog=ContactsDB;integrated security=True;MultipleActiveResultSets=True;App=EntityFramework&quot;" providerName="System.Data.EntityClient" />

3. Build the project and run it.
4. For testing consume the Web API using Postmen, Fidler, etc.


Pending work:
1. Logging
2. Unit Testing

