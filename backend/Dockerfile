# psycopg2 require python 3.6
FROM python:3.6

#ENV SECRET_KEY qwerty12345qwert12345
ARG SECRET_KEY
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client python3-dev libgraphviz-dev && rm -rf /var/lib/apt/lists/*
WORKDIR /app/backend
COPY requirements.txt /app/backend
RUN pip3 install -r requirements.txt
EXPOSE 8000
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
