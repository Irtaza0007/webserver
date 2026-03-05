# Use the official Node.js LTS image
FROM node:24.13.0

# Set working directory inside the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json first (for caching dependencies)
COPY package*.json ./

# Install only production dependencies
RUN npm install

# Copy the rest of the backend source code
COPY . .

# Expose the backend port
EXPOSE 5555

# Run the backend in production mode
CMD ["npm", "start"]