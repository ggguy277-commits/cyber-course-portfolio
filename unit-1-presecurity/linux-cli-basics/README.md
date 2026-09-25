# Part 1

## Q1 - What username are you logged in as?

Command:
```
whoami
```

Output:
```
varia
```

**Answer:** whoami outputs username of the device.

## Q2 - Are you a member of the sudo group? How can you tell from the output of id?

Command:
```
id
```

Output:
```
uid=1000(varia) gid=1000(varia) groups=1000(varia),24(cdrom),25(floppy),27(sudo),29(audio),30(dip),44(video),46(plugdev),100(users),101(netdev),102(scanner),106(bluetooth),108(lpadmin)
```
**Answer:** Yes, I am member of sudo group. It writed on "group=" line "27(sudo)".

## Q3 - What kernel version is your system running?

Command:
```
uname -a
```

Output:
```
Linux debMM 6.12.107+deb13-amd64 #1 SMP PREEMPT_DYNAMIC Debian 6.12.107-1 (2026-08-29) x86_64 GNU/Linux
```
**Answer:** Kernel version is 6.12.107+deb13-amd64

## Q4: What is the difference in the depth of information they give you?

Command:
```
whatis whoami
```

Output:
```
whoami (1)           - print effective user name
```

Command:
```
man whoami
```

Output:
```
WHOAMI(1)                        User Commands                        WHOAMI(1)

NAME
       whoami - print effective user name

SYNOPSIS
       whoami [OPTION]...

DESCRIPTION
       Print the user name associated with the current effective user ID.  Same
       as id -un.

       --help display this help and exit

       --version
              output version information and exit

AUTHOR
       Written by Richard Mlynarik.

REPORTING BUGS
       GNU coreutils online help: <https://www.gnu.org/software/coreutils/>
       Report any translation bugs to <https://translationproject.org/team/>

SEE ALSO
       Full documentation <https://www.gnu.org/software/coreutils/whoami>
       or available locally via: info '(coreutils) whoami invocation'

       Packaged by Debian (9.7-3)
       Copyright © 2025 Free Software Foundation, Inc.
       License   GPLv3+:  GNU  GPL  version  3  or  later  <https://gnu.org/li‐
       censes/gpl.html>.
       This is free software: you are free to change and redistribute it.
       There is NO WARRANTY, to the extent permitted by law.

GNU coreutils 9.7                  June 2025                          WHOAMI(1)
```

**Answer:** In addition to the name, the `man whoami` command displays: a description, a synopsis, the author, and so on.

## Q5: While in man, how do you (a) search for the word "user" and (b) quit?

Command:
```
/user
```

**Answer:** When I enter this command, the "user" text is highlighted with a black outline, and I press the "q" key to exit.

# Part 2

## Q6: What did cd - do?

**Answer:** The `cd -` command takes me back to the previous directory—that is, the folder I was in before the last change of directory.

## Q7: What additional information does -l give you over plain ls?

Command:
```
ls -l /etc
```

Output:
```
total 1076
-rw-r--r--  1 root                 root                  3981 May  6  2025 adduser.conf
-rw-r--r--  1 root                 root                    44 Sep 12 11:40 adjtime
drwxr-xr-x  3 root                 root                  4096 Sep 12 11:34 alsa
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:56 alternatives
-rw-r--r--  1 root                 root                   460 Jun  2  2025 anacrontab
drwxr-xr-x  4 root                 root                  4096 Sep 12 11:34 apache2
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:14 apparmor
drwxr-xr-x  8 root                 root                  4096 Sep 12 11:36 apparmor.d
drwxr-xr-x  9 root                 root                  4096 Sep 12 11:39 apt
drwxr-xr-x  3 root                 root                  4096 Sep 12 11:36 avahi
-rw-r--r--  1 root                 root                  1997 May  9 07:07 bash.bashrc
-rw-r--r--  1 root                 root                    45 Jan 11  2025 bash_completion
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:35 bash_completion.d
-rw-r--r--  1 root                 root                   367 Apr 27 16:09 bindresvport.blacklist
drwxr-xr-x  2 root                 root                  4096 Apr 13 15:38 binfmt.d
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 bluetooth
-rw-r--r--  1 root                 root                  7374 Jul 25  2024 bogofilter.cf
drwxr-xr-x  3 root                 root                  4096 Sep 12 11:33 ca-certificates
-rw-r--r--  1 root                 root                  6422 Sep 12 11:35 ca-certificates.conf
drwxr-s---  2 root                 dip                   4096 Sep 12 11:35 chatscripts
drwxr-xr-x  3 root                 root                  4096 Sep 12 11:34 chromium
drwxr-xr-x  2 colord               colord                4096 Sep 12 11:41 colord
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:15 console-setup
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:35 cracklib
drwx------  2 root                 root                  4096 Apr 13 15:38 credstore
drwx------  2 root                 root                  4096 Apr 13 15:38 credstore.encrypted
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:35 cron.d
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 cron.daily
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:14 cron.hourly
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:35 cron.monthly
-rw-r--r--  1 root                 root                  1042 Jun 13  2025 crontab
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 cron.weekly
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:35 cron.yearly
drwxr-xr-x  5 root                 lp                    4096 Sep 25 05:58 cups
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 cupshelpers
drwxr-xr-x  4 root                 root                  4096 Sep 12 11:33 dbus-1
drwxr-xr-x  4 root                 root                  4096 Sep 12 11:34 dconf
-rw-r--r--  1 root                 root                  2967 Mar 10  2025 debconf.conf
-rw-r--r--  1 root                 root                     5 Jul 17 13:05 debian_version
drwxr-xr-x  3 root                 root                  4096 Sep 12 11:39 default
-rw-r--r--  1 root                 root                  1706 May  6  2025 deluser.conf
drwxr-xr-x  2 root                 root                  4096 Sep 12 12:27 depmod.d
drwxr-xr-x  3 root                 root                  4096 Sep 12 11:33 dhcp
-rw-r--r--  1 root                 root                  1274 Jun 26 11:23 dhcpcd.conf
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 dictionaries-common
drwxr-xr-x  3 root                 root                  4096 Sep 12 11:56 dkms
drwxr-xr-x  4 root                 root                  4096 Sep 12 11:56 dpkg
-rw-r--r--  1 root                 root                   685 May  9 07:36 e2scrub.conf
drwxr-xr-x  3 root                 root                  4096 Sep 12 11:33 emacs
-rw-r--r--  1 root                 root                     0 Sep 12 11:14 environment
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 environment.d
-rw-r--r--  1 root                 root                  1936 Mar 15  2025 ethertypes
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 firefox-esr
drwxr-xr-x  4 root                 root                  4096 Sep 12 11:35 fonts
-rw-r--r--  1 root                 root                   806 Sep 12 11:14 fstab
-rw-r--r--  1 root                 root                   725 Jul 16  2025 fuse.conf
drwxr-xr-x  4 root                 root                  4096 Sep 12 11:36 fwupd
-rw-r--r--  1 root                 root                  2584 Jan 28  2025 gai.conf
drwxr-xr-x  6 root                 root                  4096 Sep 12 11:36 gdm3
drwxr-xr-x  3 root                 root                  4096 Sep 12 11:36 geoclue
drwxr-xr-x  4 root                 root                  4096 Sep 12 11:33 ghostscript
drwxr-xr-x  3 root                 root                  4096 Sep 12 11:33 glvnd
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:35 gnome
drwxr-xr-x  2 gnome-remote-desktop gnome-remote-desktop  4096 Sep 12 11:36 gnome-remote-desktop
-rw-r--r--  1 root                 root                  3986 Mar  3  2025 gprofng.rc
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:35 groff
-rw-r--r--  1 root                 root                   977 Sep 12 12:27 group
-rw-r--r--  1 root                 root                   959 Sep 12 12:27 group-
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:37 grub.d
-rw-r-----  1 root                 shadow                 829 Sep 12 12:27 gshadow
-rw-r-----  1 root                 shadow                 814 Sep 12 12:27 gshadow-
drwxr-xr-x  3 root                 root                  4096 Sep 12 11:14 gss
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 gtk-3.0
-rw-r--r--  1 root                 root                     9 Jul  4 05:05 host.conf
-rw-r--r--  1 root                 root                     6 Sep 12 11:14 hostname
-rw-r--r--  1 root                 root                   185 Sep 12 11:14 hosts
-rw-r--r--  1 root                 root                   411 Sep 12 11:35 hosts.allow
-rw-r--r--  1 root                 root                   711 Sep 12 11:35 hosts.deny
drwxr-xr-x  3 root                 root                  4096 Sep 12 11:35 ifplugd
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:35 ImageMagick-7
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 init.d
drwxr-xr-x  5 root                 root                  4096 Sep 12 11:14 initramfs-tools
-rw-r--r--  1 root                 root                  1875 Dec 13  2024 inputrc
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 insserv.conf.d
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 ipp-usb
-rw-r--r--  1 root                 root                    27 Jul  4 05:05 issue
-rw-r--r--  1 root                 root                    20 Jul  4 05:05 issue.net
drwxr-xr-x  8 root                 root                  4096 Sep 12 11:56 kernel
-rw-r--r--  1 root                 root                   144 Sep 12 11:39 kernel-img.conf
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:35 ldap
-rw-r--r--  1 root                 root                 74759 Sep 12 12:26 ld.so.cache
-rw-r--r--  1 root                 root                    34 Apr 27 16:09 ld.so.conf
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:56 ld.so.conf.d
-rw-r--r--  1 root                 root                    26 Feb 21  2024 libao.conf
-rw-r--r--  1 root                 root                   191 Nov 14  2024 libaudit.conf
drwxr-xr-x  3 root                 root                  4096 Sep 12 11:34 libblockdev
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:35 libnl-3
drwxr-xr-x  3 root                 root                  4096 Sep 12 11:33 libreoffice
drwxr-xr-x  4 root                 root                  4096 Sep 12 11:35 lighttpd
-rw-r--r--  1 root                 root                  2996 Apr 27 16:09 locale.alias
-rw-r--r--  1 root                 root                    54 Sep 12 11:14 locale.conf
-rw-r--r--  1 root                 root                  9580 Sep 12 11:18 locale.gen
lrwxrwxrwx  1 root                 root                    36 Sep 12 11:14 localtime -> /usr/share/zoneinfo/America/New_York
drwxr-xr-x  4 root                 root                  4096 Sep 12 11:33 logcheck
-rw-r--r--  1 root                 root                  5939 Apr 19  2025 login.defs
-rw-r--r--  1 root                 root                   494 Jul 14  2024 logrotate.conf
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 logrotate.d
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:35 lynx
-r--r--r--  1 root                 root                    33 Sep 12 11:14 machine-id
-rw-r--r--  1 root                 root                   111 Apr 11  2025 magic
-rw-r--r--  1 root                 root                   111 Apr 11  2025 magic.mime
-rw-r--r--  1 root                 root                 44535 Sep 12 11:35 mailcap
-rw-r--r--  1 root                 root                   449 Nov 11  2024 mailcap.order
-rw-r--r--  1 root                 root                  5230 May  2  2025 manpath.config
-rw-r--r--  1 root                 root                 78282 Mar  7  2025 mime.types
-rw-r--r--  1 root                 root                   813 May  9 07:36 mke2fs.conf
drwxr-xr-x  5 root                 root                  4096 Sep 12 11:35 ModemManager
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:56 modprobe.d
-rw-r--r--  1 root                 root                   212 Sep 12 11:14 modules
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 modules-load.d
-rw-r--r--  1 root                 root                   286 Jul  4 05:05 motd
lrwxrwxrwx  1 root                 root                    19 Sep 12 11:40 mtab -> ../proc/self/mounts
-rw-r--r--  1 root                 root                 11763 May  3 19:09 nanorc
-rw-r--r--  1 root                 root                   767 Mar 17  2025 netconfig
drwxr-xr-x  7 root                 root                  4096 Sep 12 11:14 network
drwxr-xr-x  8 root                 root                  4096 Sep 12 11:36 NetworkManager
-rw-r--r--  1 root                 root                    60 Sep 12 11:14 networks
-rwxr-xr-x  1 root                 root                   243 Jun 10  2025 nftables.conf
-rw-r--r--  1 root                 root                   569 Sep 12 11:35 nsswitch.conf
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:35 openal
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:35 openni2
drwxr-xr-x  3 root                 root                  4096 Sep 12 11:36 opt
lrwxrwxrwx  1 root                 root                    21 Jul 17 13:05 os-release -> ../usr/lib/os-release
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 PackageKit
-rw-r--r--  1 root                 root                   552 Jun 29  2025 pam.conf
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 pam.d
-rw-r--r--  1 root                 root                  1309 Mar 28  2025 paperspecs
-rw-r--r--  1 root                 root                  2232 Sep 12 12:27 passwd
-rw-r--r--  1 root                 root                  2187 Sep 12 11:39 passwd-
drwxr-xr-x  3 root                 root                  4096 Sep 12 11:33 perl
drwxr-xr-x  4 root                 root                  4096 Sep 12 11:33 pki
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:35 plymouth
drwxr-xr-x  3 root                 root                  4096 Sep 12 11:33 polkit-1
drwxr-xr-x  8 root                 dip                   4096 Sep 12 11:35 ppp
-rw-r--r--  1 root                 root                   828 Jul  4 05:05 profile
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:35 profile.d
-rw-r--r--  1 root                 root                  3144 Oct 17  2022 protocols
drwxr-xr-x  3 root                 root                  4096 Sep 12 11:35 pulse
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:35 python3
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:33 python3.13
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 rc0.d
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 rc1.d
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 rc2.d
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 rc3.d
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 rc4.d
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 rc5.d
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 rc6.d
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 rcS.d
-rw-r--r--  1 root                 root                  3229 Feb 19  2025 reportbug.conf
-rw-r--r--  1 root                 root                   113 Sep 25 05:57 resolv.conf
lrwxrwxrwx  1 root                 root                    13 Dec 18  2024 rmt -> /usr/sbin/rmt
-rw-r--r--  1 root                 root                   911 Oct 17  2022 rpc
drwxr-xr-x  3 root                 root                  4096 Sep 12 11:33 runit
-rw-r--r--  1 root                 root                  5772 Mar 14  2025 rygel.conf
drwxr-xr-x  3 root                 root                  4096 Sep 12 11:36 sane.d
drwxr-xr-x  4 root                 root                  4096 Sep 12 11:35 security
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:14 selinux
-rw-r--r--  1 root                 root                 10749 Apr 12  2025 sensors3.conf
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:35 sensors.d
-rw-r--r--  1 root                 root                 12990 Mar 15  2025 services
drwxr-xr-x  3 root                 root                  4096 Sep 12 11:36 sgml
-rw-r-----  1 root                 shadow                1065 Sep 12 12:27 shadow
-rw-r-----  1 root                 shadow                1043 Sep 12 11:39 shadow-
-rw-r--r--  1 root                 root                   118 Sep 12 11:19 shells
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 skel
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:35 snmp
drwxr-xr-x  4 root                 root                  4096 Sep 12 11:36 speech-dispatcher
drwxr-xr-x  4 root                 root                  4096 Sep 12 11:35 ssh
drwxr-xr-x  4 root                 root                  4096 Sep 12 11:35 ssl
-rw-r--r--  1 root                 root                    19 Sep 12 11:39 subgid
-rw-r--r--  1 root                 root                     0 Sep 12 11:14 subgid-
-rw-r--r--  1 root                 root                    19 Sep 12 11:39 subuid
-rw-r--r--  1 root                 root                     0 Sep 12 11:14 subuid-
-rw-r--r--  1 root                 root                  4337 Apr 11 08:21 sudo.conf
-r--r-----  1 root                 root                  1714 Apr 11 08:21 sudoers
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:35 sudoers.d
-rw-r--r--  1 root                 root                  9804 Apr 11 08:21 sudo_logsrvd.conf
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:14 supercat
drwxr-xr-x  3 root                 root                  4096 Sep 12 11:33 sv
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:14 sysctl.d
drwxr-xr-x  5 root                 root                  4096 Sep 12 11:35 systemd
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:14 terminfo
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:35 timidity
drwxr-xr-x  2 root                 root                  4096 Apr 13 15:38 tmpfiles.d
-rw-r--r--  1 root                 root                  1259 May 19  2025 ucf.conf
drwxr-xr-x  4 root                 root                  4096 Sep 12 11:14 udev
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 udisks2
drwxr-xr-x  3 root                 root                  4096 Sep 12 11:33 ufw
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 update-motd.d
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 UPower
-rw-r--r--  1 root                 root                  1523 Feb  1  2025 usb_modeswitch.conf
drwxr-xr-x  2 root                 root                  4096 May 24  2024 usb_modeswitch.d
lrwxrwxrwx  1 root                 root                    16 Sep 12 11:14 vconsole.conf -> default/keyboard
-rw-r--r--  1 root                 root                    51 Mar  7  2022 vdpau_wrapper.cfg
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:14 vim
drwxr-xr-x  5 root                 root                  4096 Sep 12 11:33 vulkan
n
-rw-r--r--  1 root                 root                  4942 Mar  8  2025 wgetrc
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 wpa_supplicant
drwxr-xr-x 11 root                 root                  4096 Sep 12 11:36 X11
-rw-r--r--  1 root                 root                   681 Feb 21  2025 xattr.conf
drwxr-xr-x  7 root                 root                  4096 Sep 12 11:36 xdg
drwxr-xr-x  2 root                 root                  4096 Sep 12 11:36 xml

```

**Answer:** The `-l` option stands for "long," meaning the command displays more detailed information.

## Q8: What does -a show that wasn't visible before? Name two examples from the output.

**Answer:** The `-a` option means "all," so the command displays hidden files and directories. `ls -la /etc` will append the filenames—which were hidden when the command `ls -l /etc` was entered—after the dots. `.resolv.conf` and `.pwd.lock`.

## Q9: What is the largest file in /var/log? What size is it?

Command:
```
ls -lhS /var/log
```

Output:
```
-rw-r--r--  1 root              root            819K Sep 12 11:56 dpkg.log
```

**Answer:** dpkg.log

## Q10: What was modified most recently?

Command:
```
ls -lt /var/log
```

Output:
```
-rw-r--r--  1 root              root              8192 Sep 25 05:58 wtmp.db
```

**Answer:** wtmp.db

# Part 3

## Q11: Show the command (or commands) you used.

Command:
```
mkdir -p ~/cyber-course/unit{1,2,3/{osint,recon,crypto},scratch}
```

**Answer:** 
