FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

CMD ["node", "app.js"]

# Used commands: 
# Network Creation: docker network create fav-network
# Mongo Container: docker run -d --rm --name mongodb --network fav-network mongo 
# API Container: docker run --name favorites --rm  --network fav-network -d -p 3000:3000 favorite-node:network