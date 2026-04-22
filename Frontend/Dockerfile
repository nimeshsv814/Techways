FROM node:14-alpine

# Set working directory
WORKDIR /app

# Copy dependency files first (for caching)
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy rest of the files
COPY . .

# Fix React binding issue (important for Docker)
ENV HOST=0.0.0.0
ENV PORT=3000

# Expose port
EXPOSE 3000

# Start app
CMD ["npm", "start"]