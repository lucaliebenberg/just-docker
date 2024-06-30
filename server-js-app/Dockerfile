FROM node:12-stretch

USER node

RUN mkdir /home/node/src

WORKDIR /home/node/src

COPY --chown=node:node . .

RUN npm --clean install

CMD ["node", "./index.js"]