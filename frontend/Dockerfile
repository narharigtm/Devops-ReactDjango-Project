# Use the official Node.js image from the Docker Hub
FROM node:14-alpine

# Set work directory
WORKDIR /app

# Install dependencies
COPY package.json /app/
COPY package-lock.json /app/
RUN npm install

# Copy project
COPY . /app/

# Build the app
RUN npm run build

# Install serve to serve the build
RUN npm install -g serve

# Serve the build
CMD ["serve", "-s", "build"]
