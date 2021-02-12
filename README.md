# openebs-grafana

simple chart to test OpenEBS Grafana Dashboard with auto imports



go into charts folder

enter those commands


kubectl create ns metrics

helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo add kube-state-metrics https://kubernetes.github.io/kube-state-metrics
helm repo add grafana https://grafana.github.io/helm-charts
helm repo update

you can remove the --kube-context params

helm --kube-context kubernetes-admin@kubernetes install monitor . -n metrics



Prometheus will be installed using NodePort 30004
AlterManager will be installed using NodePort 30005
Grafana will be using NodePort 30006

the user/password for Grafana is :  admin/admin







