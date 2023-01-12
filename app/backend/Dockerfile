FROM node:19-alpine3.16

ADD server /server

WORKDIR /server

RUN npm i

RUN npm run build

ENTRYPOINT ["npm", "run", "start"]