# Base image
FROM node:18

# Working directory
WORKDIR /app

# Layer
COPY package*.json ./

# COPY . .

# COPY package.json

RUN npm install

# Copy all but folders and files inside dockerignore file
COPY . .

CMD [ "npm", "start" ]