FROM node:lts-alpine
WORKDIR /app
COPY ./dist/apps/svc-cart .
COPY package.json package-lock.json ./
ENV PORT=3333
EXPOSE ${PORT}
RUN npm install --production
# dependencies that express needs
RUN npm install reflect-metadata tslib rxjs express
CMD node ./main.js


