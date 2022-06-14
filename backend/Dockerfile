FROM node:12-alpine

RUN export PATH=$PATH:/usr/local/lib/nodejs/bin

COPY --chown=node:node . /src
EXPOSE 7950:7950
ENV REFRESH=10
USER node
WORKDIR /src
RUN npm install

ENTRYPOINT ["/bin/sh", "-c", "node index.js"]