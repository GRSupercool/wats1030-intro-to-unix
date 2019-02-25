# *nix Scavenger Hunt

Complete the following challenges using the command-line interface on your favorite
Unix or Linux operating system. You are welcome and encouraged to consult any
additional documentation online or in books.

Please add your answers/responses/text pastes to the document after each prompt.

Note: For some of the challenges you will need to reference files included with
this repository, so you will need to fork the repo into your own Github account
and then clone it to your development environment.

## The Challenges

### Navigating the Filesystem

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. *Paste the output of the `pwd` command here:*
/root/wats1030-intro-to-unix

* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *What directories and files do you see when you run `ls`?*

LICENSE    challenge_files        nix_scavenger_hunt_stretch.md
README.md  nix_scavenger_hunt.md  super_scavengers.md

* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. *How are the results different when you use the `-alh` options?*  


total 40K
drwxr-xr-x 4 root root 4.0K Feb 16 21:12 .
drwx------ 6 root root 4.0K Feb 16 21:12 ..
drwxr-xr-x 8 root root 4.0K Feb 16 21:12 .git
-rw-r--r-- 1 root root 1.1K Feb 16 21:12 LICENSE
-rw-r--r-- 1 root root 2.7K Feb 16 21:12 README.md
drwxr-xr-x 7 root root 4.0K Feb 16 21:12 challenge_files
-rw-r--r-- 1 root root 5.4K Feb 16 21:12 nix_scavenger_hunt.md
-rw-r--r-- 1 root root  319 Feb 16 21:12 nix_scavenger_hunt_stretch.md
-rw-r--r-- 1 root root  255 Feb 16 21:12 super_scavengers.md


* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://man.he.net/). Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. *Write down what those options do?*  
 -a, --all
              do not ignore entries starting with .  
              
 -l     use a long listing format  
 
 -h, --human-readable
              with -l and/or -s, print human readable sizes (e.g., 1K 234M 2G)
              
          
* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. *What files and directories do you see listed?*

bin   home            lib64       opt   sbin  tmp      vmlinuz.old
boot  initrd.img      lost+found  proc  snap  usr
dev   initrd.img.old  media       root  srv   var
etc   lib             mnt         run   sys   vmlinuz


* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) *Then run `pwd` and paste the output here:*  /




* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. *Run `pwd` and paste the response here:*  /root


* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. *How many files do you find?*
-rw-r--r-- 1 root root 0 Feb 16 21:12 2015_special_stuff.demo
-rw-r--r-- 1 root root 0 Feb 16 21:12 cloaked-wookie.demo
-rw-r--r-- 1 root root 0 Feb 16 21:12 scooter-double-mamba.demo
root@wats3020:~/wats1030-intro-to-unix/challenge_files#


* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?*
root@wats3020:~#


* Press the up arrow on your keyboard. *What just happened?*
root@wats3020:~# ls -al *.demo*


* Press the up arrow a few more times. *What do you see?*
root@wats3020:~# ls -a .demo*


* Run the `history` command. *What do you see?*

 1  whoami
    2  ls
    3  https://github.com/GRSupercool/wats1030-intro-to-unix
    4  sudo apt-get install git
    5  git help -a
    6  git config --global user.name "GRSupercool"
    7  root@wats3020:~#
    8  git config --global user.name "GRSupercool"
    9  root@wats3020:~#
   10  git config --global user.email "ms.georgina.ramirez@gmail.com"
   11  git config --list
   12  ls -al ~/.ssh
   13  ssh-keygen -t rsa -b 4096 -C "ms.georgina.ramirez@gmail.com"
   14  ls -al ~/.ssh
   15  cat ~/.ssh/id_rsa.pub
   16  git clone
   17  git@github.com:GRSupercool/wats1030-intro-to-unix.git
   18  git clone git@github.com:GRSupercool/wats1030-intro-to-unix.git
   19  ls
   20  cd wats1030-intro-to-unix/
   21  ls
   22  pwd
   23  ls
   24  ls -alh
   25  man
   26  man man
   27  man ls
   28  ls /
   29  run pwd
   30  cd/
   31  cd /
   32  pwd
   33  cd
   34  cd ~
   35  pwd
   36  ls
   37  cd
   38  cd wats
   39  cd wats1030-intro-to-unix/
   40  ls -a .demo
   41  ls
   42  cd challenge_files/
   43  pwd
   44  ls
   45  ls -a
   46  ls -a .demo
   47  ls -a .demo*
   48  ls -a *.demo*
   49  ls -al *.demo*
   50  cd
   51  ls -al *.demo*
   52  ls -a .demo*
   53  r
   54  -r
   55  hostory
   56  history


### Observing the System

* Discover what account you are logged into using the `whoami` command. *What username are you currently using?*
root


* Discover who else is on your system with the `who` command. *Are any other users using your system? If so, list them here:*  
root     pts/0        2019-02-16 20:47 (73.97.141.94)


* How long has your system been running? Use `uptime` to see, and *paste the result here:*
 21:55:24 up  1:09,  1 user,  load average: 0.00, 0.00, 0.00


* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) *How do you interpret what you see here?*  
USER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root         1  0.0  0.8  77628  8540 ?        Ss   20:46   0:01 /sbin/init
root         2  0.0  0.0      0     0 ?        S    20:46   0:00 [kthreadd]
root         4  0.0  0.0      0     0 ?        I<   20:46   0:00 [kworker/0:0H]
root         6  0.0  0.0      0     0 ?        I<   20:46   0:00 [mm_percpu_wq]
root         7  0.0  0.0      0     0 ?        S    20:46   0:00 [ksoftirqd/0]
root         8  0.0  0.0      0     0 ?        I    20:46   0:00 [rcu_sched]
root         9  0.0  0.0      0     0 ?        I    20:46   0:00 [rcu_bh]
root        10  0.0  0.0      0     0 ?        S    20:46   0:00 [migration/0]
root        11  0.0  0.0      0     0 ?        S    20:46   0:00 [watchdog/0]
root        12  0.0  0.0      0     0 ?        S    20:46   0:00 [cpuhp/0]
root        13  0.0  0.0      0     0 ?        S    20:46   0:00 [kdevtmpfs]
root        14  0.0  0.0      0     0 ?        I<   20:46   0:00 [netns]
root        15  0.0  0.0      0     0 ?        S    20:46   0:00 [rcu_tasks_kthre]
root        16  0.0  0.0      0     0 ?        S    20:46   0:00 [kauditd]
root        17  0.0  0.0      0     0 ?        S    20:46   0:00 [khungtaskd]
root        18  0.0  0.0      0     0 ?        S    20:46   0:00 [oom_reaper]
root        19  0.0  0.0      0     0 ?        I<   20:46   0:00 [writeback]
root        20  0.0  0.0      0     0 ?        S    20:46   0:00 [kcompactd0]
root        21  0.0  0.0      0     0 ?        SN   20:46   0:00 [ksmd]
root        22  0.0  0.0      0     0 ?        SN   20:46   0:00 [khugepaged]
root        23  0.0  0.0      0     0 ?        I<   20:46   0:00 [crypto]
root        24  0.0  0.0      0     0 ?        I<   20:46   0:00 [kintegrityd]
root        25  0.0  0.0      0     0 ?        I<   20:46   0:00 [kblockd]
root        26  0.0  0.0      0     0 ?        I<   20:46   0:00 [ata_sff]
root        27  0.0  0.0      0     0 ?        I<   20:46   0:00 [md]
root        28  0.0  0.0      0     0 ?        I<   20:46   0:00 [edac-poller]
root        29  0.0  0.0      0     0 ?        I<   20:46   0:00 [devfreq_wq]
root        30  0.0  0.0      0     0 ?        I<   20:46   0:00 [watchdogd]
root        34  0.0  0.0      0     0 ?        S    20:46   0:00 [kswapd0]
root        35  0.0  0.0      0     0 ?        S    20:46   0:00 [ecryptfs-kthrea]
root        77  0.0  0.0      0     0 ?        I<   20:46   0:00 [kthrotld]
root        78  0.0  0.0      0     0 ?        I<   20:46   0:00 [acpi_thermal_pm]
root        79  0.0  0.0      0     0 ?        S    20:46   0:00 [scsi_eh_0]
root        80  0.0  0.0      0     0 ?        I<   20:46   0:00 [scsi_tmf_0]
root        81  0.0  0.0      0     0 ?        S    20:46   0:00 [scsi_eh_1]
root        82  0.0  0.0      0     0 ?        I<   20:46   0:00 [scsi_tmf_1]
root        88  0.0  0.0      0     0 ?        I<   20:46   0:00 [ipv6_addrconf]
root        97  0.0  0.0      0     0 ?        I<   20:46   0:00 [kstrp]
root       114  0.0  0.0      0     0 ?        I<   20:46   0:00 [charger_manager]
root       154  0.0  0.0      0     0 ?        S    20:46   0:00 [scsi_eh_2]
root       155  0.0  0.0      0     0 ?        I<   20:46   0:00 [scsi_tmf_2]
root       156  0.0  0.0      0     0 ?        I<   20:46   0:00 [kworker/0:1H]
root       253  0.0  0.0      0     0 ?        I    20:46   0:00 [kworker/0:2]
root       261  0.0  0.0      0     0 ?        I<   20:46   0:00 [raid5wq]
root       313  0.0  0.0      0     0 ?        S    20:46   0:00 [jbd2/vda1-8]
root       314  0.0  0.0      0     0 ?        I<   20:46   0:00 [ext4-rsv-conver]
root       381  0.0  0.0      0     0 ?        I<   20:46   0:00 [iscsi_eh]
root       389  0.0  0.7  78456  7280 ?        S<s  20:46   0:00 /lib/systemd/systemd-journald
root       396  0.0  0.1  97708  1832 ?        Ss   20:46   0:00 /sbin/lvmetad -f
root       399  0.0  0.0      0     0 ?        I<   20:46   0:00 [ib-comp-wq]
root       400  0.0  0.0      0     0 ?        I<   20:46   0:00 [ib_mcast]
root       401  0.0  0.0      0     0 ?        I<   20:46   0:00 [ib_nl_sa_wq]
root       402  0.0  0.0      0     0 ?        I<   20:46   0:00 [rdma_cm]
systemd+   526  0.0  0.3 141916  3128 ?        Ssl  20:46   0:00 /lib/systemd/systemd-timesyncd
systemd+   563  0.0  0.5  71960  5944 ?        Ss   20:46   0:00 /lib/systemd/systemd-networkd
systemd+   575  0.0  0.4  70616  5016 ?        Ss   20:46   0:00 /lib/systemd/systemd-resolved
root       662  0.0  0.3  42960  3960 ?        Ss   20:46   0:00 /lib/systemd/systemd-udevd
root       798  0.0  0.5  70568  6032 ?        Ss   20:46   0:00 /lib/systemd/systemd-logind
root       801  0.0  0.1  95540  1612 ?        Ssl  20:46   0:00 /usr/bin/lxcfs /var/lib/lxcfs/
root       804  0.0  0.6 287980  6732 ?        Ssl  20:46   0:00 /usr/lib/accountsservice/accounts-daemo
root       805  0.0  0.3  31748  3204 ?        Ss   20:46   0:00 /usr/sbin/cron -f
message+   807  0.0  0.4  50052  4404 ?        Ss   20:46   0:00 /usr/bin/dbus-daemon --system --address
root       822  0.0  1.9 187640 20168 ?        Ssl  20:46   0:00 /usr/bin/python3 /usr/share/unattended-
root       825  0.0  1.6 170816 17024 ?        Ssl  20:46   0:00 /usr/bin/python3 /usr/bin/networkd-disp
syslog     827  0.0  0.4 263036  4392 ?        Ssl  20:46   0:00 /usr/sbin/rsyslogd -n
daemon     830  0.0  0.2  28332  2376 ?        Ss   20:46   0:00 /usr/sbin/atd -f
root       836  0.0  0.6 288876  6516 ?        Ssl  20:46   0:00 /usr/lib/policykit-1/polkitd --no-debug
root       847  0.0  0.2  16412  2412 ttyS0    Ss+  20:46   0:00 /sbin/agetty -o -p -- \u --keep-baud 11
root       851  0.0  0.1  14888  1912 tty1     Ss+  20:46   0:00 /sbin/agetty -o -p -- \u --noclear tty1
root       935  0.0  0.6  72296  6556 ?        Ss   20:46   0:00 /usr/sbin/sshd -D
root      1056  0.0  0.7 107984  7216 ?        Ss   20:47   0:00 sshd: root@pts/0
root      1065  0.0  0.7  76620  7464 ?        Ss   20:47   0:00 /lib/systemd/systemd --user
root      1071  0.0  0.2 109312  2260 ?        S    20:47   0:00 (sd-pam)
root      1174  0.0  0.5  23200  5180 pts/0    Ss   20:47   0:00 -bash
root      1251  0.0  0.0      0     0 ?        I    21:01   0:00 [kworker/u2:1]
root      1308  0.0  0.0      0     0 ?        I    21:09   0:00 [kworker/u2:0]
root      1318  0.0  0.0      0     0 ?        I    21:09   0:00 [kworker/0:1]
root      1488  0.0  0.3  40092  3544 pts/0    R+   21:55   0:00 ps aux



* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) *How do you interpret what you see here?*

top - 21:57:24 up  1:11,  1 user,  load average: 0.00, 0.00, 0.00
Tasks:  78 total,   1 running,  43 sleeping,   0 stopped,   0 zombie
%Cpu(s):  0.0 us,  0.3 sy,  0.0 ni, 99.7 id,  0.0 wa,  0.0 hi,  0.0 si,  0.0 st
KiB Mem :  1009156 total,   709180 free,    75336 used,   224640 buff/cache
KiB Swap:        0 total,        0 free,        0 used.   792560 avail Mem

  PID USER      PR  NI    VIRT    RES    SHR S %CPU %MEM     TIME+ COMMAND
 1056 root      20   0  107984   7216   6196 S  0.3  0.7   0:00.18 sshd
 1489 root      20   0   44412   4000   3420 R  0.3  0.4   0:00.04 top
    1 root      20   0   77628   8540   6452 S  0.0  0.8   0:01.64 systemd
    2 root      20   0       0      0      0 S  0.0  0.0   0:00.00 kthreadd
    4 root       0 -20       0      0      0 I  0.0  0.0   0:00.00 kworker/0:0H
    6 root       0 -20       0      0      0 I  0.0  0.0   0:00.00 mm_percpu_wq
    7 root      20   0       0      0      0 S  0.0  0.0   0:00.07 ksoftirqd/0
    8 root      20   0       0      0      0 I  0.0  0.0   0:00.07 rcu_sched
    9 root      20   0       0      0      0 I  0.0  0.0   0:00.00 rcu_bh
   10 root      rt   0       0      0      0 S  0.0  0.0   0:00.00 migration/0
   11 root      rt   0       0      0      0 S  0.0  0.0   0:00.01 watchdog/0
   12 root      20   0       0      0      0 S  0.0  0.0   0:00.01 cpuhp/0
   13 root      20   0       0      0      0 S  0.0  0.0   0:00.00 kdevtmpfs
   14 root       0 -20       0      0      0 I  0.0  0.0   0:00.00 netns
   15 root      20   0       0      0      0 S  0.0  0.0   0:00.00 rcu_tasks_kthre
   16 root      20   0       0      0      0 S  0.0  0.0   0:00.00 kauditd
   17 root      20   0       0      0      0 S  0.0  0.0   0:00.00 khungtaskd
   18 root      20   0       0      0      0 S  0.0  0.0   0:00.00 oom_reaper
   19 root       0 -20       0      0      0 I  0.0  0.0   0:00.00 writeback
   20 root      20   0       0      0      0 S  0.0  0.0   0:00.00 kcompactd0
   21 root      25   5       0      0      0 S  0.0  0.0   0:00.00 ksmd
   22 root      39  19       0      0      0 S  0.0  0.0   0:00.00 khugepaged


### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. *How many files did you find?* two 
-rw-r--r-- 1 root root 16275 Feb 16 21:12 credit_cards.txt
-rw-r--r-- 1 root root 16240 Feb 16 21:12 credit_cards2.txt


* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) *What is the date in the file you have viewed?* 

Last updated 01-15-2015



* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. *Where is that file located?*  ./tmp/modi_laboriosam.txt



* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). *How many files did you find?*


* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. *Paste the result showing the file and line where the word "Waldo" shows up.*

### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. *What do you see in the `files.txt` file?*
* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. *Describe what you see when you run `ls -alh | more`.*
* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. *Paste the list of processes that reference your username here:*
