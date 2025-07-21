# Dockerfile

FROM node:18

# Set working directory
WORKDIR /app

# Copy dependency definitions
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy source code
COPY . .

# Default port (can be overridden by Docker/K8s)
ENV PORT=3000

# Expose port (Docker doesn't resolve $PORT at build time)
EXPOSE 3000

# Start the service
CMD ["npm", "start"]
