FROM python:3.9-slim

WORKDIR /app
COPY . .

RUN apt-get update && apt-get install -y default-libmysqlclient-dev build-essential pkg-config
RUN pip install flask flask-cors flask-mysqldb

EXPOSE 5000

ENV FLASK_APP=app

CMD ["flask", "run", "--host=0.0.0.0", "--port=5000"]