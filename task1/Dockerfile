# FROMはベースとなるコンテナのOSイメージを指定
FROM ubuntu:latest

# RUNは指定されたコマンドを実行
RUN apt-get update && apt-get upgrade -y

RUN apt-get install -y python3 python3-pip

RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

RUN pip3 install Flask

WORKDIR /app

COPY ./api.py /app/api.py

EXPOSE 5252

# CMDはコンテナ起動時に実行されるコマンド
CMD ["python3", "api.py"]
