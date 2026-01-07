FROM node:18-alpine

# Create app directory inside container
WORKDIR /app

# Copy dependency files first (for Docker cache)
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the backend code
COPY . .

# Backend listens on port 5000
EXPOSE 5000

# Start the server
CMD ["node", "index.js"]
