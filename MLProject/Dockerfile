FROM python:3.12.7-slim

WORKDIR /app

COPY requirements_docker.txt requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 5000

CMD ["mlflow", "models", "serve", "-m", "runs:/5e1956ef3a254880a264a965b801189c/model", "--host", "0.0.0.0", "--port", "5000", "--no-conda"]
