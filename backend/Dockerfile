# Use a small Node image
FROM node:18-alpine

# Create app directory
WORKDIR /usr/src/app

# Install deps first (better caching)
COPY package*.json ./
RUN npm ci --only=production

# Copy source
COPY . .

# Expose backend port
EXPOSE 5000

# Start the server
CMD ["npm", "start"]
