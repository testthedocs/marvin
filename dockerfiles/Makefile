# The shell we use
SHELL := /bin/bash

# We like colors
# From: https://coderwall.com/p/izxssa/colored-makefile-for-golang-projects
RED=`tput setaf 1`
GREEN=`tput setaf 2`
RESET=`tput sgr0`
YELLOW=`tput setaf 3`

# Add the following 'help' target to your Makefile
# And add help text after each target name starting with '\#\#'
.PHONY: help
help: ## This help message
	@grep -E '^[a-zA-Z_-]+:.*?## .*$$' $(MAKEFILE_LIST) | sort | awk 'BEGIN {FS = ":.*?## "}; {printf "\033[36m%-30s\033[0m %s\n", $$1, $$2}'

.PHONY: create-rakpart-check
create-rakpart-check: ## Creates boilerplate for a new rakpart check
	@echo "$(YELLOW)==> Creating boilerplate for new check ...$(RESET)"
	@cookiecutter -o data /srv/cookiecutters/cookiecutter-rakpart/

.PHONY: repo
repo: ## Copies default PR, Issue and Feature templates for GitHub into place
	@echo "$(YELLOW)==> Moving GitHub templates into place...$(RESET)"
	@cp -r /srv/templates/repo/.github data
