FROM registry.access.redhat.com/ubi8/python-39:1

USER root

RUN dnf update -y && dnf upgrade -y

USER 1001

WORKDIR /opt/app-root/src

COPY --chown=1001 . .

RUN pip3 install --upgrade --no-cache-dir pip urllib3 setuptools && \
    pip3 install --no-cache-dir "git+https://github.com/ibm/detect-secrets.git@master#egg=detect-secrets"
