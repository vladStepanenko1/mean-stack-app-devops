FROM node:alpine3.13
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm config set registry http://registry.npmjs.org/ && \
    npm install
COPY . .
EXPOSE 4200
CMD [ "npm", "start"]