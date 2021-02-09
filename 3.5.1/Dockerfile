FROM gcr.io/google.com/cloudsdktool/cloud-sdk:alpine

ENV HELM_VERSION="v3.5.1"

RUN gcloud components install kubectl

RUN wget -q https://get.helm.sh/helm-${HELM_VERSION}-linux-amd64.tar.gz -O - | tar -xzO linux-amd64/helm > /usr/local/bin/helm \
    && chmod +x /usr/local/bin/helm

RUN helm plugin install https://github.com/jkroepke/helm-secrets