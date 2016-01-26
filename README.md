# s3fs

This is a unofficial fork of the s3fs filesystem app (https://github.com/s3fs-fuse/s3fs-fuse). Provisions have been added so that content encoding (gzip) settings will be profiled for files in specific folders or with specific extensions.

A new parameter called gzip_folders can be set as a mount option.  If you were mounting via fstab, this is what an example mount would look like.

mybucket         /mnt/localfolder     s3fs    default_acl=public-read,use_cache=/tmp,cache_expiration=86400,gzip_folders=/source1/subfolder1:/source2/subfolder2
