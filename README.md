# Django Docker Boilerplate

A simple Django Set Up with Docker and Postgres

- pipenv shell (to create a virtual env and install dependencies)
- djangoadmin startproject <your-project-name> . 
- adjust docker-compose.yml config to match the name of your app
- adjust settings.py to add postgresql connection
- [optional]: add extra dependencies to Pipfile before running docker-compose
- docker-compose up -d --build
- docker-compose exec web python manage.py startapp <your-app-name> (initialize app from within the container)
- restart web container if it can't connect to database (docker-compose restart web)
