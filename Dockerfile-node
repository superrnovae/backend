FROM debian:9

RUN apt-get update -yq\
    && apt-get install curl gnupg -yq \
    && curl -sL https://deb.nodesource.com.setup10.x | bash \
    && apt-get installnodejs -yq \
    && apt-get clean -y

ADD . /app/

WORKDIR /app

RUN npm install

EXPOSE 2368

VOLUME /app/logs

CMD npm run start