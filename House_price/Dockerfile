FROM --platform=linux/amd64 python:3.11-slim
# Install dependencies:
RUN apt-get update
RUN apt-get install -y pip curl unzip git
# Install dependencies: Kubectl Client
WORKDIR /home
WORKDIR /app
COPY ./app /app
RUN pip install --no-cache-dir --force-reinstall -r requirements.txt
CMD ["python3","app.py"]
EXPOSE 8000