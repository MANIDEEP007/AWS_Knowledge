# AWS RDS
- RDS stands for Relational Data Service
- It is a Managed DB Service that use SQL
- Supported DB's by AWS
  - PostgreSQL
  - MySQL
  - Maria DB
  - Oracle
  - Microsoft SQL Server
  - Aurora(Amazon Proprietary DB)
# How to make RDS Single AZ to Multi AZ
- It a Zero Downtime operation and does not need to stop DB
- We just need to Modify DB properties and enable Multi zone
- Internally how this works is given below
  - Snapshot is taken from the DB
  - Another DB is restored from Snapshot
  - Synchronization is established between 2DB's
# RDS Encryption
- Snapshot of encrypted DB is Encrypted and Snapshot of Unencrypted DB is UnEncrypted
- We can make a copy of Unencrypted Snapshot as Encrypted
- Making Unencrypted DB encrypted can be done as below
- Create snapshot of DB and make Unencrypted snaphot encrypted
- Restore DB from encrypted snapshot & migrate Apps to New DB and delete old DB
