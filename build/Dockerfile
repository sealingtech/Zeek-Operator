FROM quay.io/operator-framework/ansible-operator:v0.18.1

COPY requirements.yml ${HOME}/requirements.yml
RUN ansible-galaxy collection install -r ${HOME}/requirements.yml \
 && chmod -R ug+rwx ${HOME}/.ansible || true

COPY watches.yaml ${HOME}/watches.yaml

COPY roles/ ${HOME}/roles/
