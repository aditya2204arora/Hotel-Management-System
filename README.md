
# **Hotel Management System**
Sample Spring Boot Project

# Usage
Edit the inventory file and add your slave/worker node names to inventory.
Run the playbook using the following command:
```bash
ansible-playbook installs.yml
```
Once everything is installed check if your docker images are working perfectly on local system:
```bash
docker compose up
```
Run the above command in the location: ```~/Hotel-Management-System ```


**Local Testing**

To test the code locally install the following packages:

    1. Java
    2. Maven
    3. PostgreSQL

Alter the password of the user postgres in postgreSQL to '12345'
Create a database in postgreSQL called 'hotel' and give all necessary privileges on database *hotel* to user *postgres*.
Create the jar file:
```bash
mvn clean package
```
Run the jar file:
```bash
java -jar target/Hotel.jar
```
Open your browser and enter the following URL:
```bash
http://localhost:8089/login
```
