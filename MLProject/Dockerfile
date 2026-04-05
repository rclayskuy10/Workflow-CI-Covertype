FROM python:3.12.7-slim

WORKDIR /app

COPY requirements_docker.txt requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 5000

CMD ["mlflow", "models", "serve", "-m", "runs:/e4d2c0c3f0ef49d4acd28a11f4636bd3/model", "--host", "0.0.0.0", "--port", "5000", "--no-conda"]
