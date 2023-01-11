# Implement the next steps for the actual Go-Hugo website's source code
build: ## Generate the website from markdown and config files in the 'dist/' folder
	@hugo

clean: ## Cleanup the content of the 'dist/' folder
	@rm -Rf dist/*

post: ## Create a new blog post using POST_TITLE and POST_NAME env variables
	@rm -Rf content/posts/$(POST_NAME).md
	@hugo new posts/$(POST_NAME).md
	@sed -i 's/title:.*/title: $(POST_TITLE)/' content/posts/$(POST_NAME).md
	@sed -i 's/draft:.*/draft: "false"/' content/posts/$(POST_NAME).md

lint: ## Check markdown files for any syntax mistake
	@markdownlint README.md DEPLOY.md

package: ## Create a .zip file that contains the binary of awesome api and dist directory
	@zip -r awesome-website.zip dist

help: ## Show this help usage
	@echo "Usage: make <command>"
	@cat Makefile | grep "^\w*:.*##.*" | sed 's/## //'

unit-tests: ## Run unit-tets of the project

integration-tests: ## Run integration-tests of the project

validate: ## Validate the errors on setup script
	@shellcheck setup.sh