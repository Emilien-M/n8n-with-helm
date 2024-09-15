ARG N8N_VERSION=1.58.2

FROM n8nio/n8n:${N8N_VERSION}

USER root
RUN npm install -g @kubernetes/client-node

RUN apk add --update --no-cache wget git curl bash yq openssl && \
    curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3 && \
    chmod 700 get_helm.sh && \
    ./get_helm.sh

USER node
ENTRYPOINT ["n8n"]