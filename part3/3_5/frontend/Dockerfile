
FROM node:alpine

RUN apk update && apk upgrade && apk add --no-cache \
    git curl && \
    git clone https://github.com/docker-hy/frontend-example-docker && \
    apk del git curl && \
    adduser -D app && \
    chown app /frontend-example-docker

WORKDIR /frontend-example-docker

RUN npm install

ENV API_URL=http://localhost:8000

USER app

CMD ["npm", "start"]