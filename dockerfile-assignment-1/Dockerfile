FROM node:6-alpine

RUN apk add --no-cache tini

WORKDIR /usr/src/app

COPY package.json /usr/src/app/

RUN npm install\
  && npm cache clean --force

COPY . /usr/src/app

EXPOSE 3000

CMD ["/sbin/tini", "--", "node", "./bin/www"]
