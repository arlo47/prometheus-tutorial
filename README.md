# Articles

- [blog on splitting up targets into JSON files](https://www.robustperception.io/using-json-file-service-discovery-with-prometheus/)

# Validation

## promtool

CLI tool provided by prometheus. Allows for syntax validation of config files.

https://prometheus.io/docs/prometheus/latest/command-line/promtool/

## Unit Testing Prometheus

https://prometheus.io/docs/prometheus/latest/configuration/unit_testing_rules/

## Multi Target Exporter Pattern

https://prometheus.io/docs/guides/multi-target-exporter/

## Service Discovery

Multiple SD configurations exist including azure: https://prometheus.io/docs/prometheus/latest/configuration/configuration/#azure_sd_config

Can also be managed in kuma control panel

## File Service Discovery Config

A team would need to modify 2 files to add a service to our blackbox exporter.

### blackbox config

Blackbox yml allows us to set up various modules (defining fail conditions, authentication, etc). A team would need to add a new module here, so blackbox knows what information to send.

### Prometheus File SD Config

Add the list of domains the team would like prom to send to blackbox as targets. This list of targets needs to have a label defining the module the domain is associated with.
