FROM node:11.10-alpine

MAINTAINER microvnhaxor

#RUN apk add --no-cache libc6-compat

RUN apk add --no-cache make gcc g++ python

WORKDIR /home/source/service

COPY package*.json ./

RUN npm cache clean --force \
  && npm install -g node-gyp \
  && npm install

ENV NODE_ENV production
ENV WS true
ENV PORT 3355
EXPOSE 3355

CMD [ "npm", "start"]

