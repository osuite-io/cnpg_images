version := 17.5
build:
	docker build -t ghcr.io/osuite-io/pgvector:$(version) .

login:
	@echo "$(GITPAT)" | docker login --username osuite-io --password-stdin ghcr.io

publish: login build
	docker push ghcr.io/osuite-io/pgvector:$(version)