# syntax=docker/dockerfile:1
FROM python:3.8-slim-buster

WORKDIR /app

# copy requirements.text into container and install dependancies.
COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

# Copy folder into container
COPY . .

RUN mkdir -p /mnt/data/

EXPOSE 3000

CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=3000"]
