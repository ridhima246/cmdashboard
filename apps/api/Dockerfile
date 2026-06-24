FROM python:3.12-slim

# Set working directory
WORKDIR /app


# Install Python dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy application code
COPY . .

# Railway sets PORT automatically
ENV PORT=8000
EXPOSE 8000

# Start the server using the dynamic PORT provided by Cloud Run (default 8080)
CMD uvicorn main:app --host 0.0.0.0 --port ${PORT:-8080}
