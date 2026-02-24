FROM nginx:1.29.3-alpine@sha256:b3c656d55d7ad751196f21b7fd2e8d4da9cb430e32f646adcf92441b72f82b14

ARG BUILD_DATE=1970-01-01T00:00:00Z
ARG COMMIT_SHA

LABEL org.opencontainers.image.created=$BUILD_DATE
LABEL org.opencontainers.image.authors="Samiul Saki Chowdhury"
LABEL org.opencontainers.image.revision=$COMMIT_SHA
LABEL org.opencontainers.image.vendor="Fluxus Logicae"
LABEL org.opencontainers.image.title="Fluxus Logicae Tech & Tools Radar image with nginx alpine"
LABEL org.opencontainers.image.description="Fluxus Logicae Tech & Tools Radar image with base nginx alpine image that serves a static web page."
RUN rm -rf /usr/share/nginx/html/*
COPY build/ /usr/share/nginx/html/fluxus-logicae-techradar/
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
