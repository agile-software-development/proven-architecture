FROM docker.repos.balad.ir/python:3

RUN pip install django djangorestframework
RUN pip install psycopg2
ADD . /src
CMD python /src/manage.py migrate; python /src/manage.py runserver 0.0.0.0:8080