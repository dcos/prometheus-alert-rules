# DC/OS Prometheus Alert Rules

This repository is the home of the official DC/OS Prometheus alert rules.

## Contributing

Please read the documentation on Prometheus [alerting rules][1] carefully, then
open a pull request with your changes.

Each DC/OS component or framework should have a single rule file which contains
all its alert rules. They will be passed to Prometheus via the `rule_files` 
configuration parameter.

## Severity Levels

Alerts may be configured at two severity levels, warning and critical.

Warnings should be used for alerts which will be read by a human, but are not
necessarily urgent. They would, for example, trigger an email alert. 

Critical should be used for alerts which will immediately interrupt a human.
They would, for example, trigger a pager. 

## Related Projects

- https://github.com/mesosphere/dcos-monitoring
- https://github.com/dcos/grafana-dashboards
- https://github.com/dcos/telegraf

[1]: https://prometheus.io/docs/prometheus/latest/configuration/alerting_rules/
