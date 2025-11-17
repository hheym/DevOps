FROM ubuntu:latest

RUN apt-get update && apt-get install -y python3 python3-pip && \
    pip install --break-system-packages flask requests

WORKDIR /app
COPY . .
CMD ["python3", "app.py"]
