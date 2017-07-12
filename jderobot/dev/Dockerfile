# Jderobot for developers
FROM jderobot/jderobot:dev

LABEL manteiner Aitor Martínez Fernández+aitor.martinez.fernandez@gmail.com

RUN cd && git clone https://github.com/aitormf/my-gitconfig.git && cd my-gitconfig && ./install.sh

COPY ./cloneJde.sh /root/

CMD ["bash"]
