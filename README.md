# grafana-dashboards

Set of grafana dashboards to share with all.

### How did I upload?

curl -H "Authorization: Bearer my_grafana_com_token" -XPOST -H "Accept: application/json" -F 'json=@dashboard.json' https://grafana.com/api/dashboards -v


### OPEN DISTRO ALERTS HISTORY

Dashboard number: [12875](https://grafana.com/grafana/dashboards/12875)

A dashboard to view the history of all alerts sent by opendistro alerting on the basis of Monitor, Trigger, and Severity.

For every alert sent by the [Opendistro alerting](https://opendistro.github.io/for-elasticsearch/features/alerting.html
) the document is saved in an [inbuilt index](https://opendistro.github.io/for-elasticsearch-docs/docs/alerting/settings/#alerting-indices).

- `Datasource: ElasticSearch`
- `Index name: .opendistro-alerting-alert-history-*`
- `Pattern: No pattern`
- `Time field name: start_time`
- `Version: 7.0+`

![open-distro-alerts-history1](open-distro-alert-history/images/open-distro-alerts-history1.png?raw=true)

![open-distro-alerts-history2](open-distro-alert-history/images/open-distro-alerts-history2.png?raw=true)