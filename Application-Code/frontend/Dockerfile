FROM node:19-alpine3.15 as build
WORKDIR /app
COPY package*.json /app/
COPY . .
RUN npm install

FROM node:19-alpine3.15
WORKDIR /app
COPY --from=build /app /app/
EXPOSE 3000
CMD [ "npm", "start" ]