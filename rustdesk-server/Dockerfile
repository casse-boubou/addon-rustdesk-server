ARG BUILD_FROM
ARG BUILD_ARCH

# https://github.com/hassio-addons/addon-base/releases
# hadolint ignore=DL3006
FROM $BUILD_FROM

# https://github.com/rustdesk/rustdesk-server/releases
ARG RUSTDESK_SERVER_VERSION=1.1.14

# Add Rustdesk-Server
RUN set -eux \
    apk update; \
    \
    apk add --no-cache --virtual .build-deps \
        unzip=6.0-r15 \
        ; \
    mkdir -p /opt; \
    curl -S -J -L -o /tmp/rustdesk-server.zip \
        "https://github.com/rustdesk/rustdesk-server/releases/download/${RUSTDESK_SERVER_VERSION}/rustdesk-server-linux-${BUILD_ARCH}.zip"; \
    unzip /tmp/rustdesk-server.zip -d /opt; \
    mv /opt/arm64v8 /opt/rustdesk-server; \
    rm /tmp/rustdesk-server.zip; \
    apk del .build-deps

COPY --chmod=445 rootfs /
WORKDIR /

# Build arguments
ARG BUILD_ARCH
ARG BUILD_DATE
ARG BUILD_DESCRIPTION
ARG BUILD_NAME
ARG BUILD_REF
ARG BUILD_REPOSITORY
ARG BUILD_VERSION

# Labels
LABEL \
    io.hass.name="${BUILD_NAME}" \
    io.hass.description="${BUILD_DESCRIPTION}" \
    io.hass.arch="${BUILD_ARCH}" \
    io.hass.type="addon" \
    io.hass.version=${BUILD_VERSION} \
    maintainer="Frosh" \
    org.opencontainers.image.title="${BUILD_NAME}" \
    org.opencontainers.image.description="${BUILD_DESCRIPTION}" \
    org.opencontainers.image.vendor="Frosh Home Assistant Add-ons" \
    org.opencontainers.image.authors="Frosh" \
    org.opencontainers.image.licenses="MIT" \
    org.opencontainers.image.url="https://github.com/casse-boubou/hassio-addons" \
    org.opencontainers.image.source="https://github.com/${BUILD_REPOSITORY}" \
    org.opencontainers.image.documentation="https://github.com/${BUILD_REPOSITORY}/blob/main/README.md" \
    org.opencontainers.image.created=${BUILD_DATE} \
    org.opencontainers.image.revision=${BUILD_REF} \
    org.opencontainers.image.version=${BUILD_VERSION}
