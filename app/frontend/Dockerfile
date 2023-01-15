FROM alpine:3.17

ADD website /website

RUN apk update && apk upgrade \
    && apk add bash vim npm
WORKDIR /website
#RUN sed -i 's/localhost/backend/g' ./pages/callback.tsx
# maybe needed, to check!
# RUN sed -i '/NEXT_PUBLIC_BACKEND_ENDPOINT/d' ./.env
# RUN echo "NEXT_PUBLIC_BACKEND_ENDPOINT=backend:3000" >> ./.env

RUN npm i
# RUN npx prisma migrate dev --name init
RUN npm run build

ENTRYPOINT ["npm", "run", "start", "--trace-warnings"]