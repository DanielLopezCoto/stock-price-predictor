FROM python:3.13-bookworm-slim

COPY --from=ghcr.io/astral-sh/uv:0.7.12 /uv /uvx /bin/

WORKDIR /backend

RUN apt-get update && apt-get upgrade



# RUN pip install --no-cache-dir --upgrade pip
# COPY ./requirements.txt ./
COPY uv.lock ./
# Equivalent to: pip install -r requirements.txt
RUN uv sync --locked 
# RUN pip install -r requirements.txt
COPY ./ /backend

# CMD ["uv", "run", "main.py"]
CMD ["tail", "-f", "/dev/null"]
