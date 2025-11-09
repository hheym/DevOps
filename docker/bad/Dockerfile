FROM ubuntu:latest

RUN apt-get update && apt-get install -y python3 python3-pip && \
    pip install flask requests && mkdir /app && cp -r * /app/

WORKDIR /app
COPY . .
CMD ["python3", "app.py"]
