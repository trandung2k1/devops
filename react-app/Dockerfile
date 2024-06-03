FROM node:14-alpine as builder

WORKDIR /app

COPY package*.json ./

RUN npm i

COPY . .

RUN npm run build

CMD ["node"]

FROM nginx:stable-alpine

# Copy builder to /usr/share/nginx/html
COPY --from=builder /app/build /usr/share/nginx/html

# Copy config nginx
COPY --from=builder /app/nginx/nginx.conf /etc/nginx/conf.d/default.conf

EXPOSE 3000


# To run in foreground
CMD ["nginx", "-g", "daemon off;"]