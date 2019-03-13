FROM node:6-alpine
EXPOSE 3000
RUN apk add --update tini \
    && mkdir -p /usr/src/app 

COPY package.json /usr/src/app

WORKDIR /usr/src/app

RUN npm install \
    && npm cache clean --force

COPY *.* /usr/src/app/

CMD ["/sbin/tini -- node ./bin/www"]