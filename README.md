ubuntu-cheatsheet
=================

Ubuntu commands for people who don't know Linux

## Disk Management
* Checking for disk space on available volumes: `df -h` command
* Check for size of folders in current working directory: `du -h --max-depth=1`

## File System
* Create .tar.gz / .tgz files: `tar -czvf {output.tgz} {folder}`
* Extract .tar.gz / .tgz files: `tar -xzvf {input.tgz} {path}`

* Watch a log file real-time: `tail -f {file}`

* Find files containing text: `grep -Rl {search} {path}` or case insensitive `grep -Rli {search} {path}`
* Download a file from the internet: `wget {url}`

* Back up your stuff locally: `rsync {source} {destination}`
* Back up your stuff to another server `rsync -avz -e ssh {path} {user}@{host}:{path}`

## Process Management
* Kill a process: `kill {pid}`
* See all running processes: `ps aux`
* Get PIDs of running processes under a specific name: `ps aux | grep {name}` or `ps aux | grep {name} | awk '{print $2}'`

## Cron Jobs
* Check existing cron jobs: `crontab -e`

## Networking
* What IP adress is assiged to me? `ifconfig`
* What TCP/IP ports are open and what programs are listening on them? `lsof -i -P` (needs to have lsof installed and be run as root)
* Where do I configure my network interfaces? `vi /etc/network/interfaces` then run `ifdown <interface>` and then `ifup <interface>`

## Databases
* How do I install MySQL? Stab a fork in your eye and install Postgres instead.
