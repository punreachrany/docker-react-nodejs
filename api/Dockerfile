# Use the official Node.js image with Alpine Linux for a smaller footprint
FROM node:17-alpine

# Install nodemon globally
RUN npm install -g nodemon

# Set the working directory inside the container
WORKDIR /app

# Copy only package.json and package-lock.json to leverage Docker cache
COPY package*.json ./

# Install the dependencies from package.json
RUN npm install

# Copy the rest of the application code
COPY . .

# Expose port 4000
EXPOSE 4000

# Command to start the app using nodemon
CMD ["npm", "run", "dev"]
