# Use a lightweight Node.js image as the base
FROM node:20-slim

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install

# Copy the entire application code to the container
COPY . .

# Build the TypeScript files
RUN npm run build

# Expose the application port
EXPOSE 7000

# Command to start the application
CMD ["npm", "start"]
