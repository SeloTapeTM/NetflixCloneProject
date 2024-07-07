# Use Node.js as the base image
FROM node:14

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code to the working directory
COPY . .

# Build the project
RUN npm run build

# Set the environment variable for the NetflixMovieCatalog API service URL
ENV MOVIE_CATALOG_SERVICE=http://localhost:8080

# Expose the port the app runs on
EXPOSE 3000

# Command to start the app
CMD ["npm", "start"]
