Create a new dotnet project using dotnet CLI:

1. create a new folder in the users/<yourname> directory:                                                mkdir DatingApp
2. create a new solution file DatingApp.sln file and API folder inside the DatingApp folder:             dotnet new webapi -controllers -n API
3. we have to add project to the solution:                                                               dotnet sln add API
4. in DatingApp folder run code. command, it will open the new project in VS Code         result:     ...Project `API/API.csproj` added to the solution


dotnet tool list -g   //get version 
go to nuget.org to get the needed Entity Framework (dotnet-ef) version
dotnet ef //show the list of available command-line tools
dotnet ef migrations -h // help with migrations
dotnet ef migrations add <MigrationName> -o Data/Migrations  //adds a new migration to the specific folder in Data/Migrations directory


dotnet ef database update // create/add database
dotnet ef database drop   // drop database


==================================UseCors========================================

In the Program.cs:

// Configure the HTTP request pipeline.
app.UseCors(x => x.AllowAnyHeader().AllowAnyMethod()
   .WithOrigins("http://localhost:4200", "https://localhost:4200"));


================================Git==============================================

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

=============================================================
gitignore!!!!! create gitignore file!!!
➜  DatingApp git:(master) ✗ dotnet new gitignore  
The template "dotnet gitignore file" was created successfully.

=============================================================

install Angular:
pm install -g @angular/cli@18

insall Node.js:
# installs fnm (Fast Node Manager)
winget install Schniz.fnm
# configure fnm environment
fnm env --use-on-cd | Out-String | Invoke-Expression
# download and install Node.js
fnm use --install-if-missing 22
# verifies the right Node.js version is in the environment
node -v # should print `v22.9.0`
# verifies the right npm version is in the environment
npm -v # should print `10.8.3`

=============================Angular CLI======================================
Install the Angular CLI
You can use the Angular CLI to create projects, generate application and library code, and perform a variety of ongoing development tasks such as testing, bundling, and deployment.

To install the Angular CLI, open a terminal window and run the following command:


npm install -g @angular/cli@17
On Windows client computers, the execution of PowerShell scripts is disabled by default. To allow the execution of PowerShell scripts, which is needed for npm global binaries, you must set the following execution policy:


Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
Carefully read the message displayed after executing the command and follow the instructions. Make sure you understand the implications of setting an execution policy.


Create a workspace and initial application
You develop apps in the context of an Angular workspace.

To create a new workspace and initial starter app:

Run the CLI command ng new and provide the name my-app, as shown here:


ng new my-app
The ng new command prompts you for information about features to include in the initial app. Accept the defaults by pressing the Enter or Return key.

The Angular CLI installs the necessary Angular npm packages and other dependencies. This can take a few minutes.

The CLI creates a new workspace and a simple Welcome app, ready to run.


Run the application
The Angular CLI includes a server, for you to build and serve your app locally.

Navigate to the workspace folder, such as my-app.

Run the following command:


cd my-app
ng serve --open
The ng serve command launches the server, watches your files, and rebuilds the app as you make changes to those files.

The --open (or just -o) option automatically opens your browser to http://localhost:4200/.

If your installation and setup was successful, you should see a page similar to the following.

==========================================Add Bootstrap and font-awesome==============================================

PS C:\Users\rober\Projects\DatingApp\client> npm install ngx-bootstrap boorstrap font-awesome

==========================================Adding HTTPS to Angular using mkcert=========================================

mkcert -install
create the ssl folder in the client folder

add to client/angular.json, in "build": { }:

        "serve": {
          "options": {
            "ssl": true,
            "sslCert": "ssl/localhost.pem",
            "sslKey": "ssl/localhost-key.pem"
          },