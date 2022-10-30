FROM node:19
RUN apt update
RUN apt install -y git
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime
RUN echo $TZ > /etc/timezone
RUN git clone https://framagit.org/yphil/petrolette
WORKDIR /petrolette
RUN npm install
RUN npm install pm2@latest -g
COPY . .
ENV TZ="Europe/Paris"
ENV NODE_ENV="development"
CMD ["node",  "http/server.js"]

