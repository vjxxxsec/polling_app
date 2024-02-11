## Building a Full Stack Polls app similar to twitter polls with Spring Boot, Spring Security, JWT, React and Ant Design



### Tutorials

1. **Clone the application**

	```bash
	git clone https://github.com/vjxxxsec/polling_app.git
	cd polling-app-server
	```

2. **Create MySQL database**

	```bash
	create database polling_app
	```

3. **Change MySQL username and password as per your MySQL installation**

	+ open `src/main/resources/application.properties` file.

	+ change `spring.datasource.username` and `spring.datasource.password` properties as per your mysql installation

4. **Run the app**

	You can run the spring boot app by typing the following command -

	```bash
	mvn spring-boot:run
	```

	The server will start on port 8080. 

	
5. **Add the default Roles**
	
	The spring boot app uses role based authorization powered by spring security. Please execute the following sql queries in the database to insert the `USER` and `ADMIN` roles.

	```sql
	INSERT INTO roles(name) VALUES('ROLE_USER');
	INSERT INTO roles(name) VALUES('ROLE_ADMIN');
	```

	Any new user who signs up to the app is assigned the `ROLE_USER` by default.

## Steps to Setup the React Front end app (polling-app-client)

First go to the `polling-app-client` folder -

```bash
cd polling-app-client
```

Then type the following command to install the dependencies and start the application -

```bash
npm install
npm start
```

The front-end server will start on port `3000`.

Hit this URL in browser http://localhost:3000/




App Actions:


Signup	      :    User can provide the details and create the username and password
Login	      :   User can provide username and password to login
Poll creation :	After logging in user can create the poll and give the options to select
Vote in poll  :	User can vote for the available polls
Logout	      :  User can logout from the application

NOTE:
     —> User can control the lifetime of poll.
     —> User can view the personal information provided while signing up in profile section.
     —> User can create as many polls they want.



