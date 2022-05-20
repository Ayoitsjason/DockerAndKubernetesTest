# We want to use nodejs as a base
FROM node:14

# Special directory we want to use (Container runs node inside WORKDIR)
WORKDIR /app

# Copy our package.json file into working directory
COPY package.json .

# We want to run script to download all out dependencies
RUN npm install

# Copy all files inside current folder to our folder inside our image
COPY . /app

# Expose port # to outside world (this line here is for documentation purposes, in your command line when you type Docker run -p `your local host port`:`dockers exposed port` `image`)
EXPOSE 3000

# Execute node server.js inside our image
CMD [ "node", "server.js" ]