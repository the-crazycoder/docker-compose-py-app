# syntax=docker/dockerfile:1
FROM python:3.7-alpine
WORKDIR /code
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0
RUN apk add --no-cache gcc musl-dev linux-headers
COPY require.txt require.txt
RUN pip install -r require.txt
EXPOSE 5000
COPY . .
CMD ["flask", "run"]