##FROM node:20-alpine
##
##WORKDIR /app
##
##ADD . /app
##
##RUN npm install
##
##EXPOSE 80
##
##CMD ["npm", "start"]
##
FROM node:20-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 80

CMD node server.js