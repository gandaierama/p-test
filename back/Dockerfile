FROM node:14.17.0-alpine

LABEL maintainer="danielbatistagalvao@hotmail.com"

WORKDIR /var/www/back/
RUN npm install --global pm2
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build
EXPOSE 3200


USER node

CMD [ "pm2-runtime", "start", "npm", "--", "start" ]