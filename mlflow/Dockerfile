FROM python:3.8-slim-buster
WORKDIR /usr/src/app
RUN pip install cryptography mlflow psycopg2-binary boto3 pymysql
ENV MLFLOW_S3_ENDPOINT_URL=http://storage:9000
#ENV AWS_ACCESS_KEY_ID=aaa
#ENV AWS_SECRET_ACCESS_KEY=aaaaa
CMD mlflow server \
	--backend-store-uri mysql+pymysql://MLFLOW:temporal@db:3306/DBMLFLOW \
	--default-artifact-root s3://mis.ejemplos \
    --host 0.0.0.0


	
