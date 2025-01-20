# Use an official Node runtime as a parent image
FROM node:18

# Set the working directory in the container to /app
WORKDIR /app

# Copy package.json and package-lock.json into the working dir
COPY package*.json ./

# Install ffmpeg in the container
RUN apt-get update && apt-get install -y ffmpeg

# Install packages specified in package.json
RUN npm install

# Copy app source inside the docker image
COPY . .

# Make port 3000 available
EXPOSE 3000

# Define the command to run the app using CMD (only one allowed)
CMD ["npm", "start"]