# Use a base image with Node.js installed
FROM node:14-alpine

# Set the working directory in the container
WORKDIR /react-hooks-frontend/

# Copy package.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Set environment variable for the base API URL
ENV REACT_APP_EMPLOYEE_BASE_REST_API_URL=${EMPLOYEE_BASE_REST_API_URL}

# Copy the source code
COPY . .

# Expose port 3000
EXPOSE 3000

# Command to run
ENTRYPOINT ["npm", "start"]
