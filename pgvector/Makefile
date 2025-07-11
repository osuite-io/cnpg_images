version := 17.5
build:
	docker build -t ghcr.io/osuite-io/cnpg_images/pgvector:$(version) .

login:
	@echo "$(GITPAT)" | docker login --username osuite-io --password-stdin ghcr.io

publish:
	docker push ghcr.io/osuite-io/cnpg_images/pgvector:$(version)