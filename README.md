# savacli
savacli is a command-line client for Avira's Anti-malware SDK (SAVAPI).

It interfaces with SAVAPI via TCP or UNIX domain socket and instructs SAVAPI to scan files and directories for malware. When SAVAPI has finished savacli reports the scan result.

savacli was developed by [sys4 AG](https://sys4.de). [sys4 AG](https://sys4.de) and [Avira](https://www.avira.com) are technology partners.

savacli is licensed GPLv3.

## Usage

Download the sources.

Install [future](https://pypi.org/project/future/) first if you are using Python2. You should use Python3 because Python2 has end of life on 2020-01-01.

Copy savacli.conf to /etc/savapi/savacli.conf and note the location of the logfile in savacli.conf.

Unless you run savacli as root create the logfile and set permissions to let the user, who runs savacli, write to the file.
