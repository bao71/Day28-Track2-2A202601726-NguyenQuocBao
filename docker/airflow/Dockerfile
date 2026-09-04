FROM apache/airflow:3.3.1-python3.12

ENV PIP_DEFAULT_TIMEOUT=120 \
    PIP_RETRIES=10

COPY --chown=airflow:root docker/airflow/requirements.txt /tmp/lab28-requirements.txt
RUN pip install --no-cache-dir --timeout 120 --retries 10 -r /tmp/lab28-requirements.txt

COPY --chown=airflow:root pyproject.toml README.md /opt/lab28/
COPY --chown=airflow:root src /opt/lab28/src
RUN pip install --no-cache-dir --timeout 120 --retries 10 --no-deps /opt/lab28
