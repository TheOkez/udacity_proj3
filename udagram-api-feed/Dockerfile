# Create node version to use

FROM node:12

# Create app directory 

WORKDIR /usr/src/app

# Install app dependencies 
# A wildcard is used to ensure both package.json and package-lock.json are copied where available (npm@5+)

COPY package.json ./
COPY package-lock.json ./
RUN npm ci

# Bundle the app source
COPY . .
EXPOSE 8080
CMD ["npm", "run", "prod"]


