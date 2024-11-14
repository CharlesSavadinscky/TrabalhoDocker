FROM node:alpine

#specify working directory
WORKDIR '/app'

# strategy to make sure only rebuild the image aby time we change the package.json file
#copy over only the package.json file
COPY package.json .

#run npm install to get all our dependencies
RUN npm install

#copy rest of the source code
COPY . .

#start the server
CMD ["npm", "start"]
