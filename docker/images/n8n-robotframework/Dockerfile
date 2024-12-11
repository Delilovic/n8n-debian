ARG N8N_VERSION
FROM delilovic/n8n:${N8N_VERSION}-bullseye-slim

USER root

RUN apt-get update && \
	apt-get install -y --no-install-recommends python3 python3-pip && \
    pip3 install --no-cache-dir robotframework robotframework-browser && \
    rfbrowser init &&\
    npx playwright install-deps && \
    npm install -g weaviate-client @mozilla/readability @postlight/parser

USER node