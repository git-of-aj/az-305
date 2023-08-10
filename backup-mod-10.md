> Fully consistent backups focus on the overall system's stability and integrity, capturing a snapshot where all processes have completed.
> Application-consistent backups concentrate on the proper state of the application's data and transactions, ensuring a smooth restore process without corruption or incomplete actions.
## Application-consistent backups:
Veeam
Commvault
Veritas Backup Exec
1. Database:
- mysqldump and Percona XtraBackup : For MySql
- Microsoft SQL Server: You can use SQL Server Management Studio to create backup jobs that ensure application-consistent backups.
Oracle Database: Oracle Recovery Manager (RMAN) is commonly used for creating consistent backups
- VMware Vsphere, Hyper-V
## Fully Consistent Backups:
- Fully consistent backups refer to data backups taken in a manner that ensures all changes and transactions within an application or system are properly completed and reflected in the backup.
  ## Blob Backups
  Point in time restore concept - https://learn.microsoft.com/en-us/azure/storage/blobs/point-in-time-restore-overview
- [DEMO: Point-in-time restore for block blobs](https://learn.microsoft.com/en-us/azure/storage/blobs/point-in-time-restore-manage?tabs=portal)
