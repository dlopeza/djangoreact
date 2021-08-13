# I used this images because psycopg2 require python <= 3.6 for runnig
FROM python:3.6

# Django's SECRET_KEY
ARG SECRET_KEY

# Install dependencies
RUN apt-get update && apt-get install -y --no-install-recommends postgresql-client python3-dev libgraphviz-dev && rm -rf /var/lib/apt/lists/*
WORKDIR /app/backend

# Copy and install python requiered modules
COPY requirements.txt /app/backend
RUN pip3 install -r requirements.txt

# Access port
EXPOSE 8000

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
