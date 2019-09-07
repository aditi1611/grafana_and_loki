Update Repositories

 $ helm repo add loki https://grafana.github.io/loki/chart

 $ helm repo update

Deploy Loki and Promtail to your cluster

 $ helm upgrade --install loki loki/loki-stack

To install Grafana on your cluster with helm, use the following command:

 $ helm install stable/grafana -n loki-grafana

 $kubectl port-forward  service/loki-grafana 3000:3000
 
Now,Navigate to http://localhost:3000 and login with admin and initial password as admin, then set your desired password

1)Add Loki as Data Source in Grafana -> Press Add data source button, choose Loki.

2)Add as the URL http://loki:3100 and press Save & Test

3)Click Explore icon

4)Check existing logs, just open Log labels
  You can get logs for apps, containers, instances etc 

Select any to get required logs !!!
