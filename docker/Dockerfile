FROM node:alpine3.13 as build
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

FROM nginx:1.21-alpine
COPY --from=build /usr/src/app/build /usr/share/nginx/html
COPY conf /etc/nginx/conf.d/default.conf