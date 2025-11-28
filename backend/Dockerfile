# Dockerfile for my app 
# Use a small node image
FROM node:18-alpine

# Create app directory
WORKDIR /usr/src/app

# Copy package files and install deps first (cache)
COPY package*.json ./
RUN npm install --only=production

# Copy source
COPY . .

# If you need build step (e.g., TypeScript), do it here:
# RUN npm run build

# Expose port your Express app binds (commonly 3000)
ENV PORT=3000
EXPOSE 3000

# Use a non-root user for safety (optional)
# RUN addgroup -S appgroup && adduser -S appuser -G appgroup
# USER appuser

CMD ["node", "server.js"]
# Or "npm", "start" depending on how backend is launched
