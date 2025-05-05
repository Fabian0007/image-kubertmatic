FROM --platform=linux/amd64 python:3.8-slim-buster
RUN apt-get update && apt-get install -y libgomp1 libquadmath0 && rm -rf /var/lib/apt/lists/*
WORKDIR /app
COPY requirements.txt /app
RUN pip install -r ./requirements.txt
COPY app.py /app
COPY net.params /app
CMD ["python3", "app.py"]