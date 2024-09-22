dotnet tool list -g   //get version 
go to nuget.org to get the needed Entity Framework (dotnet-ef) version
dotnet ef //show the list of available command-line tools
dotnet ef migrations -h // help with migrations
dotnet ef migrations add <MigrationName> -o Data/Migrations  //adds a new migration to the specific folder in Data/Migrations directory


dotnet ef database update // create/add database
dotnet ef database drop   // drop database

======================================================================================================================================

Git

Quick setup — if you’ve done this kind of thing before
or	
https://github.com/roberto9853/DatingApp.git
Get started by creating a new file or uploading an existing file. We recommend every repository include a README, LICENSE, and .gitignore.

…or create a new repository on the command line
echo "# DatingApp" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/roberto9853/DatingApp.git
git push -u origin main
…or push an existing repository from the command line
git remote add origin https://github.com/roberto9853/DatingApp.git
git branch -M main
git push -u origin main