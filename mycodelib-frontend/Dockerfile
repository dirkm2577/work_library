# Use an official Node.js runtime as a parent image
FROM node:14

# Set the working directory in the container
WORKDIR /mycodelib-frontend

# Copy package.json and package-lock.json into the container
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

ENV PORT=8080

# Build the app for production with minification
RUN npm run build

# Make port 8080 available to the world outside this container
EXPOSE 8080

# Run the app when the container launches
CMD ["npm", "run", "serve"]
