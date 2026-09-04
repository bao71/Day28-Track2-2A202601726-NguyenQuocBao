FROM python:3.12.11-slim

ENV PYTHONDONTWRITEBYTECODE=1 \
    PYTHONUNBUFFERED=1 \
    PIP_DEFAULT_TIMEOUT=120 \
    PIP_RETRIES=10

RUN pip install --no-cache-dir --timeout 120 --retries 10 "feast==0.66.0" "redis==6.4.0"
WORKDIR /workspace/feature-repo

EXPOSE 6566 8000
