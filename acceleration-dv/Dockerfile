FROM node

MAINTAINER sabasabarish.10@gmail.com

COPY . .

RUN yarn && \
    yarn install && \
    yarn build

EXPOSE 3001

ENTRYPOINT  ["/bin/bash", "-c"]
CMD ["yarn dev"]
