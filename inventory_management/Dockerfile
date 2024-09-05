# Your Solution
FROM python:3.10-slim

WORKDIR /app

# Copy the entire project directory
COPY . .

# Install the dependencies
RUN pip install --no-cache-dir -r inventory_management/requirements.txt

# Set the Python path to include the book_catalog directory
ENV PYTHONPATH=/app/inventory_management

# Expose port 8000
EXPOSE 9000

# Run the FastAPI app with uvicorn
CMD ["uvicorn", "inventory_management.main:app", "--host", "0.0.0.0", "--port", "9000"]