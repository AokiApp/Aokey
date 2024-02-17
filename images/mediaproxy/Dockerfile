# Using Node.js version 20
FROM node:20

# Install git
RUN apt-get update && apt-get install -y git

# make the directory
RUN mkdir -p /usr/src/app

# Set up the working directory
WORKDIR /usr/src/app

# Fetch the latest code from GitHub
RUN git clone https://github.com/misskey-dev/media-proxy.git ./

# Install dependencies
RUN npm install

# Build the application
RUN npm run build

# Set up environment variables
ENV NODE_ENV production
ENV PORT 3000

# Expose the application on port 3000
EXPOSE 3000

# Run the application
CMD [ "npm" , "start" ]
