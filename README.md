# Django Docker Boilerplate

### A simple Django Set Up with Docker and Postgres

1. Create a virtual env and install dependencies
- pipenv shell

2. Start a new Django project
- djangoadmin startproject <your-project-name> . 

3. Adjust docker-compose.yml & .env config to match the name of your app, your db, etc

4. Adjust settings.py to add postgresql connection

5. [optional]: Add extra dependencies to Pipfile before building containers:
- docker-compose up -d --build 

6. Initialize app from within the container
- docker-compose exec web python manage.py startapp <your-app-name> 

7. [optional] Restart web container if it can't connect to database (docker-compose restart web)
