Using this configuration with the start code

Make sure (first time, other wise the environment variables will not be read) your local data directory is empty. This is where the data will be persisted

Do: `docker-compose up -d`

Then: `docker container exec -it ID/name bash`
Check bind: `mysql --verbose --help | grep bind-address`
In the terminal start a mysql client:
`mysql -u root -p`

Allow remote access to the dev user:
`GRANT ALL PRIVILEGES ON *.* TO 'dev'@'%' WITH GRANT OPTION;`

Create the test database:
`CREATE DATABASE startcode_test`

Run the start code project from Netbeans

Tomcat part inspired by: https://octopus.com/blog/deployable-tomcat-docker-containers
