# dotnetcore6webapi
dot net core 6 web api example

https://docs.microsoft.com/en-us/aspnet/core/tutorials/first-web-api?view=aspnetcore-6.0&tabs=visual-studio


Test Api Using httpRepl
------------------------
HttpRepl: A command-line tool for interacting with RESTful HTTP services
https://docs.microsoft.com/en-us/aspnet/core/web-api/http-repl/?view=aspnetcore-6.0&tabs=windows

Install http-repl
------------------
dotnet tool install -g Microsoft.dotnet-httprepl

Save Item
------------
httprepl https://localhost:7087/api/todoitems
post -h Content-Type=application/json -c "{"name":"walk dog","isComplete":true}"

Get All Items
-------------
connect https://localhost:7087/api/todoitems
get

Get Item
--------------
connect https://localhost:7087/api/todoitems/1
get

Update Item
---------------
connect https://localhost:7087/api/todoitems/1
put -h Content-Type=application/json -c "{"id":1,"name":"feed fish","isComplete":true}"

Delete Item
---------------
connect https://localhost:7087/api/todoitems/1
delete