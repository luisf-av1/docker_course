FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

CMD ["node", "app.js"]

# Used commands: 
# Mongo Container: docker run -d --name mongodb mongo 
# API Container: docker run --name favorites --rm -d -p 3000:3000 favorite-node