FROM node:14

ARG DEFAULT_PORT=80

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

ENV PORT $DEFAULT_PORT

EXPOSE $PORT

# VOLUME [ "/app/node_modules" ]

CMD [ "npm", "start" ]
# docker run -d -p 3000:8080 --env-file ./.env  -v feedback:/node-app/feedback  -v /node-app/temp -v /node-app/node_modules -v $(pwd):/node-app:ro --rm --name feedback-app  feedback-node:volumes
# docker run -d -p 3000:8080 --env PORT=8080  -v feedback:/node-app/feedback  -v /node-app/temp -v /node-app/node_modules -v $(pwd):/node-app:ro --rm --name feedback-app  feedback-node:volumes
# docker run -d -p 3000:8080 -e PORT=8080  -v feedback:/node-app/feedback  -v /node-app/temp -v /node-app/node_modules -v $(pwd):/node-app:ro --rm --name feedback-app  feedback-node:volumes
# -v feedback:/node-app/feedback =  volume to save locally the changes generated after running the container
# -v $(pwd):/node-app:ro =  bind mount to detect the changes made locally, after running the container (overwrites the image build) (ro: read only, this option makes we can save files in temp or feedback folder after running the container)
# -v /node-app/node_modules = anonymous volume added to avoid overwriting the modules installation 
#-v /node-app/temp = anonymous volume added to allow the application saving (writing) inside temp folder