Backup scripts
==============
Contains scripts used to automate backing up to Amazon S3. Databases are dumped and backed up. Files are synced to a bucket which should be versioned.

Copy `config.eg` to `config`, and fill in the required info. 

Then setup a cronjob to run the `backup` script.

Dependencies
------------
- [aws-cli](http://aws.amazon.com/cli/)