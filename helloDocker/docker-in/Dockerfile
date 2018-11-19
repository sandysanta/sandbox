FROM library/centos:7

VOLUME /tmp

RUN yum install -y java; \
    useradd sandy -d /home/sandy -G users -m

### use ADD to unpack archives or use resources from URLs as input
COPY hello-docker.jar startService.sh /home/sandy/

## https://docs.docker.com/engine/reference/builder/#cmd
## CMD echo "Starting up container process with user rights ..."; \
##    su -l sandy -c ./startService.sh

ENTRYPOINT ["su","-l","sandy","-c","./startService.sh"]

