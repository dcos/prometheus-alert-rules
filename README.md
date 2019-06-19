# DC/OS Prometheus Alert Rules

This repository is the home of the official DC/OS Prometheus alert rules. They are automatically included in releases of the DC/OS Monitoring framework. 

## Contributing

Please read the documentation on Prometheus [alerting rules][1] carefully, then
open a pull request with your changes.

Each DC/OS component or framework should have a single rule file which contains
all its alert rules. They will be passed to Prometheus via the `rule_files` 
configuration parameter.

## Severity Levels

Alerts should be configured at two severity levels, warning and critical:

- **`warning`** should be used for alerts which will be read by a human, but do not
require immediate action. They would, for example, trigger an email notification. 

- **`critical`** should be used for alerts which will immediately interrupt a human.
They would, for example, trigger a pager notification. 

## Related Projects

- https://github.com/mesosphere/dcos-monitoring
- https://github.com/dcos/grafana-dashboards
- https://github.com/dcos/telegraf

[1]: https://prometheus.io/docs/prometheus/latest/configuration/alerting_rules/
