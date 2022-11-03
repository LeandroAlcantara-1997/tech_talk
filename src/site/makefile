#!/usr/bin/env make -f

appid=appratico-talks

deploy-prod:
	gcloud app deploy app.yaml \
	--project=${appid} \

deploy-branch:
	gcloud app deploy app.yaml \
	--project=${appid} \
	--version $$(git rev-parse --abbrev-ref HEAD | tr '[:upper:]' '[:lower:]') \
	--no-promote --quiet
