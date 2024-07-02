FROM node:12-stretch

RUN npm install -g nodemon

USER node

RUN mkdir /home/node/src

WORKDIR /home/node/src

COPY --chown=node:node package-lock.json package.json ./

RUN npm --clean install

COPY --chown=node:node . .

RUN npm --clean install

CMD ["nodemon", "index.js"]