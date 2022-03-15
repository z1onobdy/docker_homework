FROM node:14-alpine
WORKDIR /frontend
COPY . .
RUN npm install && npm install -g serve && npm run build
CMD ["serve", "-s", "build"]