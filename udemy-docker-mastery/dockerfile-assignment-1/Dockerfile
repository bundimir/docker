FROM node:6-alpine
EXPOSE 3000
RUN apk add --update tini \
    && mkdir -p /usr/src/app 

COPY package.json /usr/src/app/package.json

WORKDIR /usr/src/app

RUN npm install \
    && npm cache clean --force

COPY . .

CMD ["/sbin/tini", "--", "node", "./bin/www"]