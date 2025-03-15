FROM hashicorp/terraform:1.11.0

LABEL org.opencontainers.image.source="https://github.com/mulecode/tool-set-terraform"
LABEL org.opencontainers.image.description="Terraform 1.11.0 Tool-set"

WORKDIR /opt/terraform

WORKDIR /opt/app

# Updates apk
RUN apk update &&  \
    apk upgrade && \
    apk add --no-cache make=4.4.1-r2 && \
    rm -rf /var/cache/apk/*

# Default entry point
ENTRYPOINT ["/bin/terraform"]
# Default command
CMD ["--version"]
