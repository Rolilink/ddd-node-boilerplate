# Install from base nodejs image
FROM node:carbon
RUN npm install -g yarn

# Copy package.json over and install
# This will get cached so we only need to install
# if the package.json changes
WORKDIR /www
COPY package.json .
COPY .npmrc .
RUN yarn

# Copy Directory
COPY . .

# Run It!
EXPOSE 9100
CMD ["yarn", dev"]
