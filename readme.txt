Server sets 5 minutes as session to all logged in users. session is refershed whenever any request is made within 5 minutes. server unauthenticates user after 5 minutes of inactivity and user has to login again.

Steps to run application - 

1. go to stack folder. run - docker-compose up

2. initialize a terminal - run following commands

	a. docker exec -it stack_postgre_1 psql postgres postgres - "this will initialize the cli for postgres db used by application"
	b. CREATE ROLE test WITH PASSWORD 'password';
	c. ALTER USER test WITH Login;
	d. CREATE DATABASE testdb;
	
3. initialize another terminal inside the auth folder.

4. type - 'npm i'

5. type - 'sequelize db:migrate'

6. type - 'node server.js' to run the server.