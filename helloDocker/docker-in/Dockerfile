FROM library/centos:7

RUN yum install -y java; \
    useradd sandy -d /home/sandy -G users -m

COPY hello-docker.jar startService.sh /home/sandy/

CMD echo "Starting up container process with user rights ..."; \
    su -l sandy -c ./startService.sh

