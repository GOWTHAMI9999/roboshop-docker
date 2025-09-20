FROM node:20
# Create the working directory explicitly
RUN mkdir -p /opt/server
WORKDIR /opt/server
# Copy package.json and install dependencies
COPY package.json . 
RUN npm install
# Copy JS files
COPY *.js .
# Set environment variables
ENV REDIS_HOST="redis" \
    CATALOGUE_HOST="catalogue" \
    CATALOGUE_PORT=8080
# Start the app
CMD ["node", "server.js"]