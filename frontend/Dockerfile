# -----------------------
# 1️⃣ Build Stage
# -----------------------
FROM node:18-alpine AS build

# Set working directory
WORKDIR /app

# Install dependencies first (better caching)
COPY package.json package-lock.json ./
RUN npm install

# Copy source code
COPY . .

# Build optimized production files
RUN npm run build

# -----------------------
# 2️⃣ Production Stage
# -----------------------
FROM nginx:1.25-alpine

# Remove default Nginx web files
RUN rm -rf /usr/share/nginx/html/*

# Copy build output from build stage
COPY --from=build /app/build /usr/share/nginx/html

# Copy custom Nginx config (optional)
# COPY nginx.conf /etc/nginx/conf.d/default.conf

# Expose port 80
EXPOSE 80

# Start Nginx
CMD ["nginx", "-g", "daemon off;"]

