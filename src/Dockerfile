FROM node:latest as build
WORKDIR /workdir/conversor/

COPY . ./

RUN npm install

FROM node:alpine3.14 as release
COPY --from=build /workdir/conversor/ ./

CMD ["node", "server.js"]