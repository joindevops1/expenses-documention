FROM node:20.13.0-alpine3.18
EXPOSE 8080
RUN addgroup -S expenses && adduser -S expenses -G expenses
WORKDIR /opt/server
RUN chown expenses:expenses /opt/server
USER expenses
COPY package.json /opt/server/
COPY server.js /opt/server/
RUN npm install
CMD ["node", "server.js"]