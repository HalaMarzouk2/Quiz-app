# Use the official Node.js image as the base image
FROM node:20-alpine as builder

# Set the working directory to /app
WORKDIR /app

# Copy the package.json and package-lock.json files
COPY package*.json ./

# Install the dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Build the Reac
#RUN npm run build

# Use a lightweight web server to serve the built React app
#FROM nginx:alpine

# Copy the built app from the builder stage
#COPY --from=builder /app/build /usr/share/nginx/html
# Expose the port that Nginx will listen on
EXPOSE 3000

# Start app 
CMD ["npm","run","start"]