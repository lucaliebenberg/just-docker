FROM node:12-stretch

USER node

RUN mkdir /home/node/src

WORKDIR /home/node/src

COPY --chown=node:node package-lock.json package.json ./

RUN npm --clean install

COPY --chown=node:node . .

RUN npm --clean install

EXPOSE 3000

CMD ["node", "index.js"]