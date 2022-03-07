# my-helm-chart

1) helm lint helm-chart-sources/*

2) helm package helm-chart-sources/*

3) helm repo index --url https://shay79il.github.io/helm-chart/ .

4) helm repo index --url https://shay79il.github.io/helm-chart/ --merge index.yaml .
