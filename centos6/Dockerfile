FROM centos:centos6


RUN yum install -y openssh-server

# Generate sshd host keys, otherwise sshd won't start in CMD.
RUN service sshd start

EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]
