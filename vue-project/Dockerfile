FROM node:18-alpine

WORKDIR /usr/src/app

COPY package*.json ./
RUN npm install

COPY . .

# Explicitly set host and port
ENV HOST=0.0.0.0
ENV PORT=5173
ENV DOCKER=true

EXPOSE 5173

CMD ["npm", "run", "dev"]
