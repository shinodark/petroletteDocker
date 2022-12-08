FROM node:19-alpine
RUN apk update
RUN apk add git
ENV TZ="Europe/Paris"
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime
RUN echo $TZ > /etc/timezone
RUN git clone https://framagit.org/yphil/petrolette
WORKDIR /petrolette
RUN npm install -g npm@latest
RUN npm install -g pm2@latest
RUN npm install
ENV NODE_ENV="development"
CMD ["node",  "http/server.js"]

