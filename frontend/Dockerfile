# ----------------------------------------------------------------------
# STAGE 1: BUILD STAGE
# Used to compile the Angular/Node.js application assets.
# We use node:18-alpine for a stable, lightweight Node environment.
# ----------------------------------------------------------------------
FROM node:18-alpine AS build
# Set the working directory
WORKDIR /app

# Copy the dependency files first (package.json and package-lock.json)
# This layer is cached until dependencies change, speeding up future builds.
COPY package*.json ./

# FIX: Add environment variable to resolve ERR_SSL_CIPHER_OPERATION_FAILED errors
# This instructs Node.js to use a less strict SSL provider, fixing common Alpine/OpenSSL issues.
ENV NODE_OPTIONS="--openssl-legacy-provider"

# Use 'npm ci' for clean, consistent installation based on package-lock.json.
# This should work now that your local 'npm install' synchronized the lock file.


# Copy the rest of the application source code
COPY . .

# Build the application (assuming 'dist' is the output folder)
# NOTE for Angular: The output folder is often 'dist/<project-name>'
# You may need to adjust the path in the final COPY step below.
RUN npm run build

# ----------------------------------------------------------------------
# STAGE 2: PRODUCTION STAGE
# Used to serve the static built files using a very lightweight Nginx.
# ----------------------------------------------------------------------
FROM nginx:stable-alpine

# Copy custom Nginx configuration for routing (important for single-page apps like Angular)
COPY nginx.conf /etc/nginx/conf.d/default.conf

# Copy the built assets from the 'build' stage into the Nginx serving directory.
# Adjust the path below if your build output is nested (e.g., /app/dist/my-app)
COPY --from=build /app/dist /usr/share/nginx/html

# Expose the standard HTTP port 80
EXPOSE 80

# Command to start Nginx in the foreground
CMD ["nginx", "-g", "daemon off;"]