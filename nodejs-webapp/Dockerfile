FROM node:14.16.0-alpine3.13
RUN addgroup app && adduser -S -G app app
RUN mkdir /app && chown app:app /app
WORKDIR /app
RUN npm install
COPY package*.json .
USER app
COPY . .
EXPOSE 3000
CMD ["npm", "start"]