# SimpliVity

The powershell scripts here can be used to build an integration of SimpliVity backups with third party backup software. The example of the prebackup script here is build for SimpliVity backup and Veeam Availability Suite integration, but it can be adjusted for other third party backup software as needed.

The following powershell scripts are available:

- OmniStackCmds.psm1          - discontinued, replaced by
- SimpliVity-PS-Cmdlets.psm1  - SimpliVity 380 Rest API powershell commands
- createXMLbackupfile.ps1     - used to create the  XML parameter file (SvtBackupJob.xml) together with encryption key (AES.key) that is used to encrypt the password of the single-sign on user, that is needed to communicate with the OVC, the VMware vCenter and the Veeam backup server.
- Svt-VM-Backup.ps1           - single VM prebackup script  
- prebackup.ResourcePool.ps1  - prebackup script that can be used if a VMware resource pool needs to be backed up
- postbackup.ps1              - postbackup clean up script

The scripts are tested with a HPE SimpliVity 380 cluster running OmniStack 3.7.7 together Veeam Availability Suite 9.5.4


Prerequisites for the Veeam backup scripts to work:

- VMware Powershell CLI     
- Veeam Powershell Snapin must be installed on the Veeam backup server
