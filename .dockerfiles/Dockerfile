FROM python:3.13-alpine

WORKDIR app

COPY ./fastapi ./app
COPY ./requirement.txt .

RUN python3 -m venv venv
RUN source venv/bin/activate
RUN pip install -r requirement.txt

CMD cd app && uvicorn main:app --host 0.0.0.0 --reload