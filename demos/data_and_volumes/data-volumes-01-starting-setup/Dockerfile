FROM node:14

WORKDIR /node-app

COPY package.json /node-app/

RUN npm install

COPY . .

EXPOSE 80

CMD [ "node", "server.js" ]

# docker run -d -p 3000:80  -v feedback:/node-app/feedback  -v /node-app/node_modules -v $(pwd):/node-app --rm --name feedback-app  feedback-node:volumes
# -v feedback:/node-app/feedback: volume to save locally the changes generated after running the container
# -v $(pwd):/node-app: bind mount to detect the changes made locally, after running the container (overwrites the image build)
# -v /node-app/node_modules: anonymous volume added to avoid overwriting the modules installation 