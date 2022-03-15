# savacli
savacli is a command-line client for Avira's Anti-malware SDK (SAVAPI).

It interfaces with SAVAPI via TCP or UNIX domain socket and instructs SAVAPI to scan files and directories for malware. When SAVAPI has finished savacli reports the scan result.

savacli was developed by [sys4 AG](https://sys4.de). [sys4 AG](https://sys4.de) and [Avira](https://www.avira.com) are technology partners.

savacli is licensed GPLv3.

## Usage

Download the sources. savacli depends on Python's argparse package. On RedHat 6.5 (and CentOS) you will need to install it manually:

``` sh
# pip install argparse
```

As of version 0.3, you will also need the "future" package, which makes savacli Python2/3 compatible:

``` sh
# pip install future
```

Copy savacli.conf to /etc/savapi/savacli.conf and note the location of the logfile in savacli.conf.

Unless you run savacli as root create the logfile and set permissions to let the user, who runs savacli, write to the file.

## Installation on Debian 9

Dependencies for Debian 9 "stretch"

``` sh
# apt install python-future python-configparser
```
