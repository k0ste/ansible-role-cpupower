# ansible-cpupower

Linux kernel tool to tune CPU power saving related features.

## Requirements

* Ansible 3.0.0+;

## Example configuration

```yaml
---
cpupower:
# Enable cpupower service or not
- enable: 'true'
# Restart cpupower service after deploy or not
  restart: 'true'
# Install cpupower package or not
  install_package: 'true'
# 'present' (do nothing if package is already installed) or 'latest' (always
# upgrade to last version)
  package_state: 'latest'
  settings:
# Valid governors: ondemand, performance, powersave, conservative, userspace
  - governor: 'performance'
    min_freq: '2.25GHz'
    max_freq: '3GHz'
```
