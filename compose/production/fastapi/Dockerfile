FROM python:3.9

WORKDIR /code

COPY ./requirements.txt /code/requirements.txt

RUN pip install --no-cache-dir --upgrade -r /code/requirements.txt

COPY ./compose/local/fastapi/start /start

RUN sed -i 's/\r$//g' /start
RUN chmod +x /start

COPY ./app /code/app