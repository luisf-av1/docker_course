FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

CMD ["node", "app.js"]

# Used command: docker run --name favorites --rm -d -p 3000:3000 favorite-node