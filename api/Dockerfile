FROM node:7.5.0

# Create app directory
RUN mkdir -p /usr/src/app

WORKDIR /usr/src/app
RUN npm install -g yarn
COPY package.json yarn.lock ./
RUN yarn install

# Bundle app source
COPY . /usr/src/app/

# Install app dependencies

EXPOSE 8000

ENTRYPOINT [ "node", "start.js" ]