FROM python:3.9-slim

COPY . .

RUN apt-get update && apt-get install -y \
    build-essential \
    curl \
    software-properties-common \
    git \
    && rm -rf /var/lib/apt/lists/*

RUN pip3 install -r requirements.txt


EXPOSE 8502

CMD ["streamlit", "run", "app.py",\
     "--server.port=8502", "--server.address=0.0.0.0"]