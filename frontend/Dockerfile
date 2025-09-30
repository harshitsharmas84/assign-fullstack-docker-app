# Use Node.js 14 Alpine as base image for smaller size
FROM node:14-alpine

# Set working directory in the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json (if available) from src directory
COPY src/package*.json ./

# Install dependencies
RUN npm install

# Create the src and public directories in the container
RUN mkdir -p src public

# Copy index.js to src directory
COPY src/index.js ./src/

# Copy app.js to src directory
COPY src/app.js ./src/

# Copy public files to public directory
COPY src/public/ ./public/

# Expose port 3000 (default React development server port)
EXPOSE 3000

# Define the command to run the application
CMD ["npm", "start"]
