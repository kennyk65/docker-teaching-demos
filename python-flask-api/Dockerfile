# syntax=docker/dockerfile:1.4
FROM python:3.10-alpine AS builder

WORKDIR /app

COPY requirements.txt /app
RUN --mount=type=cache,target=/root/.cache/pip \
    pip3 install -r requirements.txt

COPY . /app

ENTRYPOINT ["python3"]
CMD ["app.py"]
# Build with:  docker build -t demo/flask-api:1 .
# Run this with:  docker run -dp 80:5000 demo/flask-api:1