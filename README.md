# bin
Some scripts I've made

---

### ccppp

For Create C Plus Plus Project

Juste a tool that will create basic files for a C++ project.
Nothing more, nothing less.

---

### lxc-up / down

My scripts for starting / stopping containers.

usage :
```
lxc-up `container-name`
lxc-down `container-name`
```
dependancies :
 - softs : sshfs, tmux
 - ssh properly configured, with .ssh/config file and key authentication.

Lxc up:
 - Starts the container `container-name`.
 - Mounts the remote homedir on ~/sshfs/`containername` with sshfs.
 - Creates a tmux session, named `container-name`.
 - Creates a first window in the tmux session named "CODE".
 - Creates a second one, named "SERVER" logged into the container through SSH.
 - Creates a third one, named "TUN", and open a SSH tunnel.
   Here, the tunel targets the postgres default bind port.
   You can change this, depending of your need, as the localhost port.

Lxc-down:
 - Kills the tmux session.
 - Unmount the sshfs mountpoint.
 - Stops the container.

---

### pg-cli

Just a wrapper of the pgcli postgres client.

Usage:
```
pg-cli <container-name> <db-name>
```

Requirements :
 - [pgcli](https://github.com/dbcli/pgcli)
 - a /tmp/pg_table file filled by the [lxc-up](https://github.com/mmequignon/bin/blob/master/lxc-up) script.
 - SSH properly configured.

It allows me to connect on a remote database, available on `localhost`
through a SSH tunnel.

 - It uses the `/tmp/pg_table` created by the `lxc-up` script
   to get the port to connect on.
 - It gets the username to connect with in your `~/.ssh/config` file.

---

### paph

A script that generates a random set of words.
It comes with `words_alpha.txt` that comes from [this repo](https://github.com/dwyl/english-words).
Both script and dict files should be placed in the same diretory.

It's role is to provide random passphrases.
Usage:
  - paph : prints 6 random words (default value)
  - paph 12 : prints 12 random words
  - paph -h : shows help
