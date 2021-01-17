
FROM node:alpine AS build-stage

RUN apk update && apk upgrade && apk add --no-cache \
    git curl && \
    git clone https://github.com/docker-hy/frontend-example-docker

WORKDIR /frontend-example-docker

ENV API_URL=http://localhost:8000

RUN npm install && npm run build


FROM node:alpine

COPY --from=build-stage /frontend-example-docker/dist ./frontend-example-docker/dist

WORKDIR /frontend-example-docker

RUN adduser -D app && \
    chown app /frontend-example-docker && \
    npm install -g serve

USER app

CMD ["serve", "-s", "-l", "5000", "dist"]