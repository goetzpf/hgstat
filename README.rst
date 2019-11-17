======
hgstat
======

A Simple shell script to display the overall state of a mercurial repository

Usage of hgstat
---------------

hgstat is invoked with::

  hgstat [OPTIONS]

All OPTIONS except the following ones are passed to the 'hg' command::

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

Usage of hgstatall
------------------

This is script calls hgstat for all mercurial scripts that it finds in and below the current working directory.

Usage::

  hgstatall [OPTIONS]
  
All OPTIONS given are passed to the "hgstat" command. See "hgstat" above.

  

