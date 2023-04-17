FROM node:14

EXPOSE 8080

WORKDIR /opt/server/
RUN addgroup catalogue && adduser --system catalogue && usermod -aG catalogue catalogue
RUN chown -R catalogue:catalogue /opt/server/
USER catalogue
COPY package.json /opt/server/
# npm install get the dependencies of the node js project .
RUN npm install
RUN ls -ltr
COPY server.js /opt/server/

CMD ["node","server.js"]



