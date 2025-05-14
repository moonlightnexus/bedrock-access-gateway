FROM python:3.12-slim

WORKDIR /app

COPY ./src/api ./api
COPY ./src/requirements.txt .

RUN pip3 install -r requirements.txt -U --no-cache-dir
RUN pip3 install uvicorn fastapi

RUN echo '#!/bin/bash\nuvicorn api.app:app --host 0.0.0.0 --port 8800' > /app/entrypoint.sh
RUN chmod +x /app/entrypoint.sh

EXPOSE 8800

CMD ["/app/entrypoint.sh"]