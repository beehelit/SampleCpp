FROM ubuntu:22.04

COPY install-deps.sh /
RUN sh install-deps.sh

# SSH
EXPOSE 22
RUN echo "StrictHostKeyChecking=no" >> /etc/ssh/ssh_config
RUN mkdir /var/run/sshd
CMD ["/usr/sbin/sshd", "-D"]
