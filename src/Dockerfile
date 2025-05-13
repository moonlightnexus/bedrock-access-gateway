FROM public.ecr.aws/lambda/python:3.12

COPY ./src/api ./api

COPY ./src/requirements.txt .

RUN pip3 install -r requirements.txt -U --no-cache-dir

CMD [ "api.app.handler" ]