# [Create Helm chart repo](https://medium.com/@mattiaperi/create-a-public-helm-chart-repository-with-github-pages-49b180dbb417)


## 1) Copy new helm-chart into `helm-chart-sources` directory
## 2) Lint
```bash
helm lint helm-chart-sources/*
```
## 3) Package
```bash
helm package helm-chart-sources/*
```
## 4) Index
```bash
helm repo index --url https://shay79il.github.io/helm-chart/ --merge index.yaml .
```
## 5) Commit changes to repo 
```bash
git add . && git commit -m “Upgrade charts” && git push origin master
```

## 6) Configure helm client
```bash
helm repo add <repo-name> https://<username>.github.io/helm-chart/
```

## 7) Upgrade changes to repo 
```bash
helm upgrade -i <release-name> <repo-name>
```