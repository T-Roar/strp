# Base image
FROM node:14-alpine

# Create app directory
WORKDIR /app

# Install app dependencies
COPY package*.json ./
RUN npm install --only=production

# Bundle app source
COPY . .

# Set environment variables
ENV PORT=3000

# Expose port
EXPOSE ${PORT}

# Start the app
CMD ["npm", "start"]