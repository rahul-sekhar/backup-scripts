Backup scripts
==============
Contains scripts used to automate backing up to Amazon S3. Databases are dumped and backed up. Files are synced to a bucket which should be versioned.

Copy `config.eg` to `config`, and fill in the required info.

Then setup a cronjob to run the `backup` script.

AWS IAM Permissions
-------------------
For the contents of the database backup bucket(`arn:aws:s3:::bucket/*`), `s3:PutObject`
For the contents of the files backup bucket(`arn:aws:s3:::bucket/*`), `s3:PutObject`, `s3:DeleteObject`
For the files backup bucket(`arn:aws:s3:::bucket`), `s3:ListBucket`

Dependencies
------------
- [aws-cli](http://aws.amazon.com/cli/)
