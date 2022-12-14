FROM python:3.7-alpine AS builder
EXPOSE 8000
WORKDIR /app
RUN apk update && apk upgrade && apk add bash 
ENV PYTHONUNBUFFERED=1
COPY requirements.txt /app
RUN pip3 install -r requirements.txt --no-cache-dir
COPY . /app 
# ENTRYPOINT ["python3"] 
# CMD ["manage.py", "runserver", "0.0.0.0:8000"]