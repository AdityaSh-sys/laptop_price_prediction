FROM python:3.12.9-slim-bullseye

# Set environment variables
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

# Set working directory
WORKDIR /app

# Copy your project files into the container
COPY ./project_root /app

# Make script executable and run it
RUN chmod +x /app/lib_install.sh && /app/lib_install.sh

# Expose the app port
EXPOSE 80

# Start the FastAPI app
CMD ["uvicorn", "inference:app", "--host", "0.0.0.0", "--port", "8000"]