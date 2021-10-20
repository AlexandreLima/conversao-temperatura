FROM node:latest as build
ENV NODE_VERSION 16.11.1
WORKDIR /workdir/path/

COPY . ./

RUN npm install

FROM node:alpine3.14 as release
COPY --from=build /workdir/path/ ./

CMD ["node", "server.js"]