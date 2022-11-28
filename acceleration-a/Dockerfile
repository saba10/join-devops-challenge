FROM node as stage1

COPY . .

RUN yarn install && \
    yarn build


FROM node:slim

MAINTAINER sabasabarish.10@gmail.com

COPY --from=stage1 /dist /dist
COPY --from=stage1 package.json ./

EXPOSE 3002

ENTRYPOINT  ["/bin/bash", "-c"]
CMD ["WEB_PORT=3002 yarn start"]
