ARG N8N_VERSION
FROM delilovic/n8n:${N8N_VERSION}-bullseye-slim

USER root

RUN apt-get update && \
    apt-get install -y --no-install-recommends python3 python3-pip curl && \
    pip3 install --no-cache-dir robotframework robotframework-browser && \
    npx playwright install-deps && \
    rfbrowser init

# Add any additional npm libraries here if required
RUN npm install -g weaviate-client @mozilla/readability @postlight/parser

USER node
