Here is the list of currently supported DETERLab operating system images. If you have a DETERLab account, you can view the most updated information as well as statistics on each machine on the <a href="https://www.isi.deterlab.net/showosid_list.php3">OSID page</a> on the testbed.

## Supported OS Images as of 07/15/2015 
  

| Name | OS | Description |
| ------- | ------ | -------------- |
| FBSD10-STD | FreeBSD | FreeBSD 10.x Standard |
| FBSD8-STD | FreeBSD | FreeBSD 8.x Standard |
| FBSD9-64-STD | FreeBSD | FreeBSD 9.x Standard |
| CentOS5 | Linux | More or less current version of CentOS 5 |
| CentOS6-64-STD | Linux | CentOS6 64-Bit image |
| KALI1 | Linux | Kali Penetration Testing |
| Metasploitable2 | Linux | An intentionally vulnerable system |
| Ubuntu1004-STD | Linux | Ubuntu 10.04 LTS Standard Image |
| Ubuntu1204-64-STD | Linux | Ubuntu 12.04 LTS 64 bit Standard Image |
| Ubuntu1404-32-STD | Linux | Ubuntu 14.04 LTS 32 bit Standard Image |
| Ubuntu1404-64-STD | Linux | Ubuntu 14.04 LTS 64 bit Standard Image |
| WINXP-UPDATE | Windows | Windows XP with SP3 and patches |

## Updates for Custom Images

### Updating Linux images made before Jan 25, 2013

We made a change to make mounting NFS home directories more robust.  You may update your custom images by running:

```
sudo curl --output /usr/local/etc/emulab/liblocsetup.pm boss.isi.deterlab.net/downloads/client-update/linux-liblocsetup.pm
sudo chmod a+rx /usr/local/etc/emulab/liblocsetup.pm
```

and taking a snapshot.  

On CentOS-6-64-STD you must to install Time::HiRes by running:

```
sudo yum install perl-Time-HiRes
```