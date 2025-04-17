# Use official Node.js base image
FROM node:latest

# Set working directory
WORKDIR /app

# Copy package.json and lock file first (better for caching)
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the app
COPY . .

# Build isn't required for dev server
# Just expose React dev server port
EXPOSE 3000

# Run React dev server
CMD ["npm", "start"]
