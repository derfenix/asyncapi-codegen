.PHONY: clean
clean: ## Clean remains of run
	@$(MAKE) -C helloworld/nats clean
	@$(MAKE) -C ping/nats clean
	@$(MAKE) -C ping/kafka clean

.PHONY: run
run: ## Run the examples
	@$(MAKE) -C helloworld/nats run
	@$(MAKE) -C ping/nats run
	@$(MAKE) -C ping/kafka run

.PHONY: help
help: ## Display this help message
	@awk 'BEGIN {FS = ":.*?## "} /^[a-zA-Z_\/-]+:.*?## / {printf "\033[34m%-30s\033[0m %s\n", $$1, $$2}' $(MAKEFILE_LIST) | \
		sort | \
		grep -v '#'
