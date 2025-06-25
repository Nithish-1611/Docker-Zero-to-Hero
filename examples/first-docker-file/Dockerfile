FROM python:3.11-slim

# Set working directory
WORKDIR /app

# Copy only necessary files first (improves layer caching)
COPY requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the app code
COPY . .

# Set environment variable
ENV NAME World

# Run the app
CMD ["python3", "app.py"]
