# Use NodeJS base image
FROM node:13

# Create app directory in Docker
WORKDIR /usr/src/app

# Install app dependencies by copying
# package.json and package-lock.json
COPY package*.json ./
#COPY udagram-api-user/package*.json /usr/src/app/
#COPY src/. /usr/src/app # this is to bring server.ts one level up

# Install dependencies in Docker

#RUN npm install
RUN npm ci

#RUN npm run build

# Copy app from local environment into the Docker image
COPY . .

# Set the API’s port number
EXPOSE 8080

# Define Docker’s behavior when the image is run
#CMD ["node", "server.js"]
CMD [ "npm", "run", "prod" ]
