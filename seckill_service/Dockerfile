FROM node:8.1.0-slim

# Create app directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# Bundle app source
COPY ./package.json /usr/src/app/
RUN npm i -s

# Bundle app source
COPY . /usr/src/app

ENV NODE_ENV=production

RUN npm run build

CMD [ "npm", "start" ]