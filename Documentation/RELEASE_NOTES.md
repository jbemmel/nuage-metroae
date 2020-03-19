# Metro Automation Engine Release Notes

## Release 4.0.0

### Feature Enhancements

* Refactor metroae command to support container management; RPM no longer required.
* Introduce day-zero VSD configuration support via `metroae config` (container only)
* Add support for Multiple VSC underlay VPRNs (MetroAE-1175)
* Add support for VSD disk I/O testing using sysbench (METROAE-1169)
* Add VSC hardening (METROAE-1183)
* Add support for VSD certificate renewal standalone procedure (METROAE-1188)
* Add support for setting up Zabbix health monitoring on compatible VSP components.
* Bash tab-completion support for metroae command
* Add VSD cluster RTT tests with configurable threshold (METROAE-766)
* Add support for VSTAT standby only deployment (METROAE-1081)
* Add discovery of existing components in wizard for KVM and vCenter
* Add option to backup and restore the /etc/host file on VSD during upgrade (METROAE-1187)
* Add support for zero factor bootstrapping multi uplinks for NSGvs (METROAE-852)
* Add support for downloading the container from S3 in tar format (METROAE-1210)

### Resolved Issues

* Fix VSC examples to have valid system ip address (METROAE-1177)
* Fix NTP retries masking non NTP sync errors (METROAE-1153)
* Fix fallocate failure on path with symbolic link (METROAE-1167)
* Fix deprecated task and changed result format for vmware_vm_facts (METROAE-1179)
* Detect when unresolved jinja2 is present in inventory (METROAE-820)
* Check for required disk space on VSD for backup files during upgrade health check (METROAE-1182)
* Fix issue with VSD failover procedure with Active Standby VSTATs (METROAE-1061)
* Convert shell mkdir tasks to ansible file module (METROAE-1059)
* Add optional user prompt confirmation before destroying components (METROAE-868)
* Improved debugging output for vCenter ovftool commands (METROAE-981)
* Vastly improved predeploy roles for code reuse (METROAE-801)
* Moved default reports directory out of playbooks and into metro root directory (METROAE-879)
* Get the debug log script working with container (METROAE-1202)
* Prevent presence of upgrade.yml from causing install to fail (METROAE-1161)
* No longer error if patch upgrade includes non-VSD components

### Removed

* Removed obsolete os_vsd_osc_integration playbook and associated role and files.
