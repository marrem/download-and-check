# download-and-check
Simple batch script to download from url and run checksum against downloaded file

Dependencies:

* bash
* curl
* md5 (usually found on MacOs / OSX)
* md5sum (usually found on Unix like systems)

```
addis:testmd5check marc$ ./downloadAndCheck ftp://ftp.xs4all.nl/pub/test/10mb.bin
md5 binary: md5
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 10.0M  100 10.0M    0     0  9643k      0  0:00:01  0:00:01 --:--:-- 9651k
MD5 (10mb.bin) = 0c7914d75e7b8a9dff2eafe6d4cda8a6

addis:testmd5check marc$ ls -l
total 20496
-rw-r--r--  1 marc  staff  10485760 May  2 20:50 10mb.bin
-rw-r--r--  1 marc  staff        50 May  2 20:50 10mb.bin.md5
-rwxr-xr-x  1 marc  staff       373 May  2 20:28 downloadAndCheck

addis:testmd5check marc$ cat 10mb.bin.md5 
MD5 (10mb.bin) = 0c7914d75e7b8a9dff2eafe6d4cda8a6

```
