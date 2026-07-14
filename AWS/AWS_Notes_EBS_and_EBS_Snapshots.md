# AWS Notes -- Amazon EBS & EBS Snapshots

## Amazon EBS

-   EBS is a block storage service for EC2.
-   Stores Operating System, applications, databases and application
    data.
-   Acts like a virtual hard disk attached to EC2.
-   Provides persistent storage.

### Persistent Storage

-   Stopping an EC2 instance does not delete data on EBS.
-   Starting the EC2 again brings back the OS, applications and data.

### Stop vs Terminate

-   Stop: EC2 stops, EBS remains.
-   Terminate: EC2 is deleted. By default the root EBS volume is also
    deleted because Delete on Termination = Yes.
-   If Delete on Termination = No, the EBS volume survives and can be
    attached to another EC2.

### Recovering EC2

1.  Launch a new EC2.
2.  Attach the existing EBS volume.
3.  Recover the OS, applications and data.

## Amazon EBS Snapshot

-   Snapshot is a point-in-time backup of an EBS volume.
-   Snapshots are stored internally in Amazon S3.
-   They do not appear as normal S3 buckets.

### Incremental Snapshots

-   First snapshot stores the full volume.
-   Later snapshots store only changed blocks.
-   Benefits: lower cost, less storage, faster backups.

## EBS vs S3

  EBS                        S3
  -------------------------- ---------------------------------------
  Block storage              Object storage
  Attached to EC2            Independent AWS service
  Stores OS & applications   Stores files, images, videos, backups

## Interview Questions

1.  What is EBS?
2.  What is persistent storage?
3.  What happens to EBS when EC2 is stopped?
4.  What is Delete on Termination?
5.  What is an EBS Snapshot?
6.  Where are snapshots stored?
7.  What is an incremental snapshot?
8.  EBS vs S3?
