FROM 192.168.33.211:5000/node-pm2
ENV APPNAME=APPService
RUN pwd
RUN cd . && ls
COPY . /opt/$APPNAME
RUN cd /opt/ && ls
RUN cd /opt/$APPNAME && ls
RUN node -v
RUN pm2 -v
WORKDIR /opt/$APPNAME