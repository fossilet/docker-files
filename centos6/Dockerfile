FROM centos:centos6

RUN yum install -y openssh-server sudo

# Generate sshd host keys, otherwise sshd won't start in CMD.
RUN service sshd start
WORKDIR /root
RUN mkdir .ssh && chmod 700 .ssh
RUN echo "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDDT07kSYwv/PcZgzkKEk4/jWjWeeLW9RnMPHpkuab6HYRMrvGJFv3niorId/1F9u6LOhvDUDAwwfv9WnxzVg+r706DQiqFc+DzUHmbA2ait6Wt5WDVhQ0/H/4xttY/Nh1zoCbzj+YQMyee2I1Hn3VNN5+7Esl64TfKcXCaqmdhtGvPw3gDSo70b+4Tc4NLN8heiKs5YFN5u8aIh7sC/uOAi9MQ/d0cmeNr1Ap1/R1vU1OnocWK1/pNcPibrrVorWc1yH58RZw3GlHVtPytQfeBCrZ6VepaDqGT35GI68H2X4Hk+dmyS5gTzg/JpWgiXPT64q+JXwRf4k9uchpzB7pV tux@YongzhiPans-MacBook-Pro.local ">> .ssh/authorized_keys

EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]
