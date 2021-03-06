# Unix Commands

These are the more common commands I use when working with Ubuntu.

## SSH (Remote connection)

- `ssh root@[ip]` - connects to a remote server (DigitalOcean!)

## Screen

- `screen` - opens the program screen (run node from here or it dies when you exit ssh)
- `screen -d -r [number]` - detach and resume the screen (use this to access that node process again after killing ssh)
- `ctrl`+`a`+`d` - exit screen view and return to primary terminal
- `screen -ls` - list current screens (don't do this inside the screen :P)
- `screen -X -S [number] quit` - kill one of those screens (`X` sends the command to the screen, `S` declares the screen session to send it to.)

## SCP

- `scp` - secure copy!
- `scp root@[ip]:[path] [local path]` - copy a file from remote to local.
- `scp [local path] root@[ip]:[path]` - copy a file from local to remote.

## File System

### Navigation

- `cd [path]` - Change directory. Can use relative or absolute path.
- `ls` - lists files
- `ls -lah` - lists `a`ll files (including dotfiles) in `l`ong format (with date edited and sizes) and `h`uman readable. Optionally sort by `t`ime.

### Editing

- `mkdir [name]` - Create folder.
- `touch [name]` - Create file.
- `[command] > [file]` - print results of command to file.
- `nano [file]` - opens text editor to write to file. Shortcuts listed on screen. Exit shortcut will prompt for save!
- `rm [file]` - delete file
- `rm -rf [directory]` - delete folder
- `cp [old path] [new path]` - copy file from old path to new path. Need to move folder? Use `-r` flag.
- `mv [old path] [new path]` - move file/folder from old path to new path

### Disk Usage

- `du -sh ./**` - Creates a `h`uman readable printout of `s`ummarized directory sizes within the current working directory. Use this for sizes over `ls` as `ls` caps at 4KB.

## Other

- `ps aux` - `ps` lists all of the processes, the `aux` flag makes a readable format. When a node process gets "stuck", use this to list them.
- `kill <pid>` - Kill the process with the `PID` from the above command.
- `su` - Switch to super user.
- `su <username>` - Switch to `username` user.
- `netstat -tulpn` - Shows current ports in use. `t` shows TCP ports, `u` shows UDP ports, `l` shows ports that are listening, `p` shows the PID (usefull to `kill`), and `n` removes the name.
