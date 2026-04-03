# Use correct Node version
FROM node:20

WORKDIR /app

# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy all files
COPY . .

# IMPORTANT: Generate Prisma client
RUN npx prisma generate

# Build TypeScript
RUN npm run build

# Expose backend port (change if needed)
EXPOSE 5000

# Start backend server
CMD ["npm", "start"]

