FROM node:14

EXPOSE 8080

WORKDIR /opt/server/
RUN addgroup catalogue && adduser --system catalogue && usermod -aG catalogue catalogue
RUN chown -R catalogue:catalogue /opt/server/
USER catalogue
COPY package.json /opt/server/
RUN ls -ltr
# npm install get the dependencies of the node js project .
RUN npm install
COPY server.js /opt/server/

CMD ["node","server.js"]


FROM node:14
EXPOSE 8080
WORKDIR /opt/server
RUN addgroup cart && adduser --system cart && usermod -aG cart cart
RUN chown -R cart:cart /opt/server/
USER cart
COPY package.json /opt/server/
RUN ls -ltr
RUN npm install
COPY server.js /opt/server/
CMD ["node","server.js"]
