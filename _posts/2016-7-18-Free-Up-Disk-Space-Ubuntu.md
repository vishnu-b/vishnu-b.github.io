---
layout: post
title: Freeing Up Disk Space Ubuntu!
---
1. Find the deleted and still open files.
  sudo lsof -h | grep deleted
2. Find the suspected process id(1060) here and list the files.
  ls -l /proc/1060/fd
3. Send the file to /dev/null. 9 is the id of the file here.
  cat /dev/null >  /proc/1060/fd/9
