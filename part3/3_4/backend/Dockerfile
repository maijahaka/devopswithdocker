
FROM node:alpine

RUN apk update && apk upgrade && apk add --no-cache \
    bash git curl shadow && \
    git clone https://github.com/docker-hy/backend-example-docker && \
    useradd -m app && \
    chown app /backend-example-docker

WORKDIR /backend-example-docker

RUN npm install

ENV FRONT_URL=http://localhost:5000

USER app

CMD ["npm", "start"]
