FROM node:14.14.0-alpine

USER node
RUN mkdir -p /home/node/app
WORKDIR /home/node/app

COPY --chown=node:node package.json .
# RUN npm install
RUN yarn install

# since we're using a volume we might as well delete this (leaving it here for prod)
COPY --chown=node:node . .

CMD ["npm", "run", "start"]