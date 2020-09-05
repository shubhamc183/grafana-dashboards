# grafana-dashboards

Set of grafana dashboards to share with all.

### How did I upload?

curl -H "Authorization: Bearer my_grafana_com_token" -XPOST -H "Accept: application/json" -F 'json=@dashboard.json' https://grafana.com/api/dashboards -v


### OPEN ALERTS OF ALERTMANAGER

Dashboard number :point_right: [12947](https://grafana.com/grafana/dashboards/12947)

A Dashboard to visualize only Open(LIVE) Alerts of AlertManager instead of looking in Slack, Teams, and Emails.

Thanks to [camptocamp](https://github.com/camptocamp) organization for [grafana-prometheus-alertmanager-datasource](https://github.com/camptocamp/grafana-prometheus-alertmanager-datasource) making Alertmanager behave like a datasource for Grafana.

This dashboard gives a holistic view of alerts in an organization that can be used by the Monitoring team. Also, provides drill down to one team's environment which can be used by the on-call person of that team.

The dashboard provides filtering on the basis of
- `region`
- `severity`
- `alert`
- `team`
- `environment`

**NOTE**: Please feel free to modify these filter labels as these are very specific to my use case or remove from the query.

![open-alerts-alertmanager](open-alerts-alertmanager/images/open-alerts-alertmanager.png?raw=true)


### OPEN DISTRO ALERTS HISTORY

Dashboard number :point_right: [12875](https://grafana.com/grafana/dashboards/12875)

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