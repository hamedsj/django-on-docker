FROM python:3.8-alpine

ENV SECRET_KEY 71)0c2pluviivk1!p93qouc_w017(#%x#g+2(*eo(0sf6h)vq3

ENV DEBUG 1

ENV ALLOWED_HOSTS web1

COPY ./requirements.txt /home

RUN pip install -r /home/requirements.txt

COPY . /home

WORKDIR /home/prj

CMD ["gunicorn", "--bind", "0.0.0.0:8080", "prj.wsgi"]
