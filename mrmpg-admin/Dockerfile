# Use Node image
FROM node:20

# Create working directory
WORKDIR /app

# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy project files
COPY . .

# Build the project
RUN npm run build

# Expose Vite preview port
EXPOSE 4173

# Run the production preview server
CMD ["npm", "run", "preview", "--", "--host"]

