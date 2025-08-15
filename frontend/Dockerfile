FROM node:18-alpine

WORKDIR /usr/src/app

# Install deps first
COPY package*.json ./
RUN npm install

# Copy app
COPY . .

# Make the dev server reachable from outside the container
ENV HOST=0.0.0.0
ENV PORT=3000
EXPOSE 3000

# Start CRA dev server
CMD ["npm", "start"]
