FROM alpine:latest 
MAINTAINER snafrutz <piermarco.zerbini@gmail.com> 
RUN apk add --update --no-cache openssh-client ansible && \
    python -m ensurepip && \
    pip install --upgrade pip && \
    pip install --upgrade boto3 && \
    pip install --upgrade Jinja2 && \
    pip install --upgrade pyvmomi && \
    pip install --upgrade ec2 && \
    pip install --upgrade awscli && \
    pip install --upgrade dopy && \
    export PATH=~/.local/bin:$PATH

ENV PATH /root/.local/bin:$PATH
ENTRYPOINT ["ansible-playbook"]
VOLUME ["/etc/ansible"]
WORKDIR /etc/ansible
