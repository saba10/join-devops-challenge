FROM node

MAINTAINER sabasabarish.10@gmail.com

COPY . .

RUN yarn && \
    yarn install && \
    yarn build

EXPOSE 3002

ENTRYPOINT  yarn dev
