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

Example
-------

Sample output (the actual output is with colors)::

  =================================================
  Repository in /home/goetz/shared/repos/vimwiki
  -------------------------------------------------
  uncomitted (hg status):
  M Bookmarks.wiki
  M Keyboard shortcuts.wiki
  ? index.wiki.orig
  -------------------------------------------------
  applied patches (hg qapplied):
  -------------------------------------------------
  unapplied patches (hg qunapplied):

  -------------------------------------------------
  outgoing mq repository patches (hg outgoing):
  comparing with ssh://goetzp@devel.home/shared/repos/vimwiki/.hg/patches       
  searching for changes
  no changes found
  -------------------------------------------------
  incoming mq repository patches (hg incoming):
  comparing with ssh://goetzp@devel.home/shared/repos/vimwiki/.hg/patches       
  searching for changes
  no changes found
  -------------------------------------------------
  outgoing patches (hg outgoing):
  comparing with ssh://goetzp@devel.home/shared/repos/vimwiki       
  searching for changes
  no changes found
  -------------------------------------------------
  incoming patches (hg incoming):
  comparing with ssh://goetzp@devel.home/shared/repos/vimwiki       
  searching for changes
  no changes found
  =================================================


  

