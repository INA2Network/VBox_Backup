# VBox_Backup
VirtualBox VM Backup Script

# Dependencies:
MariaDB-shared.x86_64
percona-xtrabackup-24

# Paths:
/db_backup - local backups path
/var/spool/cron/root - cron job for root
/root/backup/ - backup scripts here
/root/.xtrabackup.config - config for xtrabackup script
/var/log/db_backup.log - log of xtrabackup script
# The following installs the yum repo file, and the GPG key
rpm -Uhv http://www.percona.com/downloads/percona-release/percona-release-0.0-1.x86_64.rpm
# Once complete, you can run the following command and select your version of percona-xtrabackup
yum search all percona

# Your new repo is located:
/etc/yum.repos.d/Percona.repo

yum install percona-xtrabackup-24

# Shell scripts and xtrabackups config written and provided by kosfango with reference to vitobotta
# kosfango is an excellent sysadmin and I hire him regularly through the UpWork platform
