FROM python:3.12-slim

WORKDIR /app

# Tell Railway exactly where the files are hiding!
COPY apps/api/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY apps/api/ .

CMD uvicorn main:app --host 0.0.0.0 --port ${PORT:-8080}
