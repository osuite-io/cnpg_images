FROM ghcr.io/cloudnative-pg/postgresql:17.5

LABEL org.opencontainers.image.source=https://github.com/osuite-io/cnpg_images
LABEL org.opencontainers.image.description="CNPG image with pgvector extension for PostgreSQL 17.5"
LABEL org.opencontainers.image.licenses=MIT
LABEL org.opencontainers.image.vendor="osuite.io"

USER root

RUN set -xe; \
	apt-get update; \
	apt-get install -y --no-install-recommends \
		"postgresql-17-pgvector" ; \
	rm -fr /tmp/* ; \
	rm -rf /var/lib/apt/lists/*;

# Change to the uid of postgres (26)
USER 26
