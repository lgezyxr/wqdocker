FROM node

RUN apt-get update && apt-get install -y curl git xsel

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app
RUN npm install -g serve
ENV CLI_WIDTH 80
RUN git clone https://github.com/lgezyxr/wqfrontend /usr/src/app
RUN npm install
RUN npm run build

EXPOSE 3000
COPY entrypoint.sh ./entrypoint.sh
CMD ["./entrypoint.sh"]
