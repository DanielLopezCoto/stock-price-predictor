FROM python:3.11-slim

WORKDIR /backend

RUN apt-get update && apt-get install
RUN pip install --no-cache-dir --upgrade pip
COPY ./requirements.txt ./
RUN pip install -r requirements.txt
COPY ./ /backend

CMD ["python", "main.py"]
