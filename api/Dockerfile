# Backend Dockerfile
FROM node:16-alpine

WORKDIR /app
RUN npm install tsconfig-paths typeorm reflect-metadata pg entities
# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy source code
COPY . .

# Build the app (if using TypeScript)
RUN npm run build 

# Expose port
EXPOSE 12345

# Start the server
CMD ["npm", "start"]
