FROM python:3.11.0a1-alpine3.14
WORKDIR /src

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY src/ .

ENTRYPOINT ["uvicorn", "--host", "0.0.0.0", "/src/server:app", "--reload"]

# ------- Comands to run -------
# docker build -t myimage app/
# docker iamges
# docker run -rm myimage

# FROM python:3.11.0a1-alpine3.14
# COPY . usr/src/app
# WORKDIR /usr/src/app
# 
# RUN pip install -r requirements.txt
# 
# ENTRYPOINT uvicorn --host 0.0.0.0 main:app --reload
