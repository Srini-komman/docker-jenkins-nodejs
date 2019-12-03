FROM node:10.16.0

ADD ./package.json /tmp/

RUN cd /tmp/ && npm install

RUN npm install -g pm2

ADD ./ /code/

RUN cp -r /tmp/node_modules/ /code/

EXPOSE 3900

WORKDIR /code

ENTRYPOINT [ "pm2-docker", "index.js" ]