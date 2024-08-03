FROM python:3.9-slim
ENV PYTHONUNBUFFERED=1
WORKDIR /code 
COPY requirements.txt /code/
RUN pip install -r requirements.txt
COPY . /code/
CMD [ "gunicorn","--bind","0.0.0.0:8000","project.wsgi:application" ]
