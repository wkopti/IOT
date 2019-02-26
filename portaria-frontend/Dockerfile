FROM nodered/node-red-docker
USER root
COPY flows.json /data/
RUN chown node-red:node-red /data/flows.json
RUN chmod 777 /data/flows.json
RUN npm install node-red-contrib-mongodb2 node-red-contrib-objectid