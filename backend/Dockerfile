# Use the official Node.js v24.13.0 image
FROM node:24.13.0

# Set working directory inside the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json first (for caching dependencies)
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the backend source code
COPY . .

# Expose the backend port (5555)
EXPOSE 5555

# Start the backend server
CMD ["npm", "start"]