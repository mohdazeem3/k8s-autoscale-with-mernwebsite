# -----------------------
# 1️⃣ Base image
# -----------------------
FROM node:18-alpine

# Set working directory
WORKDIR /app

# -----------------------
# 2️⃣ Install dependencies
# -----------------------
# Copy only dependency files first for better caching
COPY package*.json ./
RUN npm install --production

# -----------------------
# 3️⃣ Copy source code
# -----------------------
COPY . .

# -----------------------
# 4️⃣ Expose API port
# -----------------------
EXPOSE 5000

# -----------------------
# 5️⃣ Start server
# -----------------------
CMD ["node", "server.js"]

