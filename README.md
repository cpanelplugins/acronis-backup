The plugin integrates WHM and cPanel with Acronis Backup or Acronis Cyber Cloud. With the plugin, a WHM user can:

- Back up an entire cPanel server to the cloud storage with the disk-level backup
- Recover the entire server including all of the websites
- Perform granular recovery of websites, individual files, mailboxes, mail filters, mail forwarders, accounts, and databases, including the databases created outside of WHM
- Enable self-service recovery for cPanel accounts once the plugin is installed and configured, the server is backed up on a predefined schedule.

A backup can also be started on demand. The backup schedule can be configured in the Acronis web console. Recovery can be performed from the WHM and cPanel interfaces. It is not possible to back up individual websites. However, the rights for self-service recovery can be granted to each account separately.

---

## System requirements

- PHP version 5.6 or later.
- Granular recovery of databases is supported only for local MySQL. Granular recovery of PostgreSQL databases is not supported.
- Besides the plugin, a backup agent must be installed on the same machine. If cPanel is running on a Virtuozzo container, the backup agent must be installed on the Virtuozzo host instead of the container.

---

## License

An Acronis Cyber Cloud or Acronis WHM and cPanel 12.5 subscription is required to use the plugin.

You can purchase an Acronis Cyber Cloud subscription from service providers.

To purchase an Acronis WHM and cPanel 12.5 subscription, visit https://www.acronis.com/business/backup/linux-server
A 30-day trial is available.

You will obtain a link and user name and password for the Acronis web console.


## Installing the plugin

To install the Acronis WHM and cPanel plugin for WHM and cPanel, run the following command:

```sh <(curl -L https://download.acronis.com/ci/cpanel/stable/install_acronis_cpanel.sh || wget -O - https://download.acronis.com/ci/cpanel/stable/install_acronis_cpanel.sh)```

Setup instructions: https://dl.acronis.com/u/pdf/Acronis_Backup_plugin_for_cPanel_en-US.pdf


---

## Uninstalling the plugin

To uninstall the Acronis Backup plugin for WHM and cPanel, run the following command:

```yum remove acronis-backup-cpanel```

Removing the extension will also uninstall the backup agent from the cPanel server. The backup accounts you created and the backed-up data will be left intact.

---

## Enable Self-Service Recovery

To enable self-service recovery for cPanel users, Acronis Backup must be enabled in for them in Feature Manager.
