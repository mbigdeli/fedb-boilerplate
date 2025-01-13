# Development stage
FROM node:20-alpine

WORKDIR /opt/app

# Copy package files first for better caching
COPY package*.json ./

# Install dependencies with legacy peer deps for compatibility
RUN npm install --legacy-peer-deps

# Copy source code
COPY . .

# Expose port
EXPOSE 3001

# Start in development mode with host setting
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"] 