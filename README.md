# helm-chart


# Step 1
Create Repo in github and clone it to your local machine 
```
git clone https://github.com/anikpujan/helm-chart.git && cd helm-chart/
```
# Step 2
Copy the directory that has helm chart contents and create helm chart package
```
cd ./test-chart
helm lint test-chart/
helm package test-chart/ 
```
# Step 3
Create the Helm chart repository index
```
helm repo index --url https://anikpujan.github.io/helm-chart/ .
```
# Step 4
Push to github repo
```
git add . && git commit -m “Initial commit” && git push origin main
```
# Step 5
Go back to your browser, in the “settings” section of your git repository, scroll down to Github Pages section and go to "Source" and choose the branch your repo is in.
Now you will see your site in which you can use to share with others. You can use the follwing command to see the repo in action:
```
helm repo add myrepo https://anikpujan.github.io/helm-chart/
helm search repo myrepo
helm install test myrepo/test-chart
```
