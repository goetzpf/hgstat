======
hgstat
======
Simple shell script to display the overall state of a mercurial repository

Usage
-----

All command line options except the following are
passed to the 'hg' commands::

  -h : this help
  -R DIRECTORY : 
       operate on repository in DIRECTORY
  -l --local : local mode, do not check for incoming and outgoing patches
  -b --brief : just check if there are uncomitted/incoming/outgoing patches
       omit any details
  -r REPO :
       define the full URL/PATH of a remote repository
  --rmq REPO :
       define the full URL/PATH of a remote mq repository
  --lmq :
       do not check remote mq repo even if local mq repo exists
  --debug :
       set tracing on
