FROM node:18-alpine

# added to support superset liveness probe
RUN apk update && apk upgrade && \
    apk add --no-cache curl

WORKDIR /usr/src/app

COPY package*.json ./
RUN npm install
COPY . .

CMD [ "npm", "start" ]
