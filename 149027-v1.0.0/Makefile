.DEFAULT_GOAL=help
.PHONY: run build clean help
PORT?=3333
HOST?=127.0.0.1
display_errors?=1
TARGET = index.php


run: $(TARGET) ## Run the test case
	php -S $(HOST):$(PORT) -d display_errors=$(display_errors) '$(TARGET)'

build: $(TARGET) ## Build the test case
	php -l '$(TARGET)'

$(TARGET): .installed

clean: ## Clean the test case

.installed: ## Install the dependencies
	sh install-dependencies.sh

help: ## Show this help
	@grep -E '^[a-zA-Z0-9_-]+:.*?## .*$$' $(MAKEFILE_LIST) | sort | awk 'BEGIN {FS = ":.*?## "}; {printf "\033[36m%-30s\033[0m %s\n", $$1, $$2}'
