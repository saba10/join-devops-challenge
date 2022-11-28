FROM node AS stage1

COPY . .

RUN yarn install && \
    yarn build


FROM node:slim

MAINTAINER sabasabarish.10@gmail.com

COPY --from=stage1 /dist /dist
COPY --from=stage1 package.json ./

EXPOSE 3001

ENTRYPOINT  ["/bin/bash", "-c"]
CMD ["WEB_PORT=3001 yarn start"]
