FROM node:alpine

WORKDIR /usr/app

# It's always a good practice to separate out the various phases of our docker build to be able to effectively use our build cache.
# Here we are splitting our two build phases into
# 1. installing the dependencies
# 2. Copy the source over to the container

# Build phase 1
COPY ./package.json ./
RUN npm install

# Build phase 2
COPY ./ ./

CMD ["npm", "start"]