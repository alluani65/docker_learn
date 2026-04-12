# 1. Choose a lightweight Python base image
FROM python:3.11-slim

# 2. Set the working directory inside the container
WORKDIR /app

# 3. Copy just the requirements file first (this helps Docker cache your dependencies)
COPY requirements.txt .

# 4. Install the Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# 5. Copy the rest of your application code into the container
COPY . .

# 6. Document that the container uses port 5000
EXPOSE 5000

# 7. Define the command that runs when the container starts
CMD ["python", "app.py"]