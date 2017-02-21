FROM alpine:latest 
MAINTAINER snafrutz <piermarco.zerbini@gmail.com> 
RUN apk add --update --no-cache openssh-client ansible && \
    python -m ensurepip && \
    pip install --upgrade pip && \
    pip install --upgrade Jinja2 && \
    export PATH=~/.local/bin:$PATH

ENV PATH /root/.local/bin:$PATH
ENTRYPOINT ["ansible-galaxy"]
VOLUME ["/etc/ansible"]
WORKDIR /etc/ansible
