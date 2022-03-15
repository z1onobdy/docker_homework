FROM python:3.10.2-alpine3.15
WORKDIR /app
COPY . .
RUN apk add --update-cache \
    python3-dev libxml2 libxml2-dev libxslt-dev libpq-dev gcc cython musl-dev \
  && pip install --upgrade pip \
  && pip install -r requirements.txt --no-cache-dir \
  && pip install psycopg2-binary \
  && rm -rf /var/cache/apk/* \
  && dos2unix cmd.sh
CMD ["/app/cmd.sh"]
