FROM python:3.10-slim

ENV PYTHONDONTWRITEBYTECODE=1

ENV PYTHONUNBUFFERED=1

ENV HABITAT="container"
ENV PRODUCT_STAGE="development"

ENV VAR1="docky"


RUN mkdir -p /container_app/lode/source_code
COPY ./requirements.txt /container_app/lode/requirements.txt

WORKDIR /container_app/lode
RUN python3 -m pip install -r requirements.txt



WORKDIR /container_app

RUN adduser -u 5678 --disabled-password --gecos "" appuser && chown -R appuser /container_app

USER appuser 

CMD ["bash"]

