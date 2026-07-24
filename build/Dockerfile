FROM python:3.10-slim

# Install MLflow and AWS SDK
RUN pip install mlflow boto3 psycopg2-binary

WORKDIR /app

EXPOSE 5000
CMD ["mlflow", "server", "--host", "0.0.0.0", "--port", "5000", "--backend-store-uri", "sqlite:////tmp/mlflow.db", "--default-artifact-root", "s3://ml-arghya-data"]

