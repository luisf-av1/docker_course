FROM node

WORKDIR /node_app

#Copy all of the files in the current working directory to the root or working directory of the image
COPY . .

#RUN: Execute the command when the image is created
RUN npm install 

EXPOSE 80

#CMD: Execute the command when the container is started based on the image
CMD ["node", "server.js"] 