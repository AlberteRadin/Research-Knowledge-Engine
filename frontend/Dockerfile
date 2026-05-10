FROM node:18-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install --production

COPY . .
RUN npm run build

EXPOSE 80
CMD ["sh", "-c", "npm install && cp -R /app/public/* /usr/share/nginx/html && nginx -g 'daemon off;' "]
