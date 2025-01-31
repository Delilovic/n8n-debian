ARG N8N_VERSION
FROM delilovic/n8n:${N8N_VERSION}-bullseye-slim

USER root

RUN apt-get update && \
    apt-get install -y --no-install-recommends python3 python3-pip curl && \
    pip3 install --no-cache-dir \
        robotframework==7.2 \
        robotframework-browser==19.3.0 && \
    npx playwright install-deps && \
    rfbrowser init

# Install Node.js packages
RUN npm install -g \
        weaviate-client@3.3.6 \
        @mozilla/readability@0.5.0 \
        @postlight/parser@2.2.3

USER node
