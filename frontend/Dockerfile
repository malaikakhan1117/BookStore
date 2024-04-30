# Use an official Node runtime as a parent image
FROM node:14

# Set the working directory
WORKDIR /usr/src/app

# Copy package.json and package-lock.json (if available)
COPY package*.json ./

# Install dependencies
RUN npm install

# Bundle app source
COPY . .

# Build the application
RUN npm run build

# Expose port 3000 or any other port used by your frontend
EXPOSE 3000

# Use serve to serve the static files
RUN npm install -g serve
CMD ["serve", "-s", "build", "-l", "3000"]
