# helm-chart

# Create the Helm chart package
```
helm package test-chart/*
```
# Create the Helm chart repository index
```
helm repo index --url https://anikpujan.github.io/helm-chart/ .
```
# Push the git repository on GitHub
```
git add . && git commit -m "Initial commit" && git push origin main
```
# Configure the “helm-chart” repository as a Github pages site
Go back to your browser, in the “settings” section of your git repository, scroll down to Github Pages section and select the branch like main or gh-pages.
# Test the Helm chart repository
```
helm repo add myrepo https://anikpujan.github.io/helm-chart/
helm search myrepo

```
