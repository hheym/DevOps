FROM python:3.11-slim

RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential && \
    rm -rf /var/lib/apt/lists/*

RUN useradd -m appuser

WORKDIR /home/appuser/app
COPY --chown=appuser:appuser requirements.txt .
USER appuser

RUN pip install --no-cache-dir --break-system-packages -r requirements.txt

COPY --chown=appuser:appuser . .

CMD ["python", "app.py"]
