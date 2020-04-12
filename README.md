# Proman_Project_Upgrad
This project explains the working of REST APIs including Controller, DAO, Services

# Step 1
Install Postgres latest version on Mac

# Step 2
Install PgAdmin client latest version on Mac

# Step 3
Clone or download the Stub project given in the Upgrad Project (or create a new repository to start the project)

# Step 4
Start the Postgres service by using below commands below:

Start manually:
pg_ctl -D /usr/local/var/postgres start

Stop manually:
pg_ctl -D /usr/local/var/postgres stop

Start automatically:
"To have launchd start postgresql now and restart at login:"
brew services start postgresql

# Step 5
Create a local configuration file with localhost properties as below:

//localhost.properties
#environment properties for local development
server.host=localhost
server.port=5432
database.name=proman
database.user=postgres
database.password=password

# Step 6
Configure the important configuration details in application.yaml file

# Step 7
Run mvn clean install in the parent module. This will automatically create the model classes by building on the Swagger based JSON files.

For each feature, there is a different JSON file.
It will create all the model classes inside the Target folder once the building is complete.
Move those files into the proman-api package (parallel to the controller or config package hierarchy).

# Step 8
Create a DB through command line or directly from the PGAdmin client tool, where the name of DB is used as "quora" as given in localhost.properties file.

# Step 9
Run the maven profile activation command (mvn clean install -Psetup) from within the DB module.

# Step 10
Run the Main application file: PromanApiApplication class

# Step 11
This will host the application on localhost:8080
To check out all the Swagger information, use below address:

http://localhost:8080/api/swagger-ui.html

![alt text](http://url/to/img.png)
