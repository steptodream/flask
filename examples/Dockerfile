FROM python:3.7

COPY ./tutorial /tutorial
WORKDIR /tutorial

ENV FLASK_APP=flaskr
ENV FLASK_ENV=development

RUN pip install --upgrade pip && pip install -e .

RUN groupadd flaskapp && useradd -g flaskapp flaskapp
USER flaskapp

EXPOSE 5000

CMD ["sh", "-c", "flask init-db | flask run --host 0.0.0.0" ]

