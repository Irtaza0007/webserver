# Use the official Node.js v24.13.0 image
FROM node:24.13.0

# Set working directory inside the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json first (for caching dependencies)
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the frontend source code
COPY . .

# Expose the frontend port (5173)
EXPOSE 5173

# Start the frontend server (Vite default)
CMD ["npm", "run", "dev", "--", "--host"]