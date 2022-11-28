FROM node

MAINTAINER sabasabarish.10@gmail.com

COPY . /opt/
WORKDIR /opt/

RUN yarn install && \
    yarn build

EXPOSE 3000

ENTRYPOINT  ["/bin/bash", "-c"]
CMD ["yarn dev"]

