FROM python:3.8-slim
WORKDIR /app

RUN apt-get update && apt-get install -y --no-install-recommends \
        pkg-config default-libmysqlclient-dev build-essential \
    && rm -rf /var/lib/apt/lists/*

COPY . .
RUN pip install flask mysqlclient
EXPOSE 5000
CMD ["python", "app.py"]
