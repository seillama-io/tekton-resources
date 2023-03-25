FROM registry.access.redhat.com/ubi8/python-39:1

USER 1001

WORKDIR /opt/app-root/src

COPY --chown=1001 . .

RUN pip3 install --no-cache-dir detect-secrets==1.4.0
