# Development stage
FROM node:20-alpine

WORKDIR /opt/app

# Copy package files first for better caching
COPY package*.json ./

# Install dependencies and NestJS CLI globally
RUN npm install && \
    npm install -g @nestjs/cli nodemon ts-node

# Copy source code
COPY . .

# Create dist directory and set permissions
RUN mkdir -p dist && \
    chown -R node:node /opt/app

# Switch to non-root user
USER node

# Expose port
EXPOSE 3000

# Start in development mode with nodemon
CMD ["nodemon"] 