LArPix Backup Software
=====================

This software will help back up LArPix data files (or, really, any files
whatsoever). This operation runs 100% on rsync.

Operation
----------

Operation is as easy as 1 2 3:

 1. In the larpix-backup base directory, create a new file called
 SOURCE_DIR which contains as its only text the absolute path to the
 directory you want to back up. Include a trailing slash if you want the
 directory contents copied but not the directory itself. Omit the
 trailing slash for the directory plus contents to be copied.

 2. In the larpix-backup base directory, create a new file called DEST
 which contains as its only text the location to copy the new files. This
 could be e.g. ``user@remote.com:path/from/home``,
 ``user@remote.com:/absolute/path``, or even just
 ``/absolute/path/on/same/computer``. If a password is required there will be
 an interactive prompt.

 3. Ensure that the file permissions are set correctly with ``chmod u+x
 backup``, then just execute ``./backup``. The progress will be displayed in
 real time.
