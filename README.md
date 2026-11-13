[README.md](https://github.com/user-attachments/files/34824366/README.md)# linux-command-line-basics
# Linux & Command Line Basics — DevOps Project 1

My first DevOps practice project, completed using Linux through Windows Subsystem for Linux (WSL). I used the terminal to create an application directory structure, write and read a log message, rename a file, and inspect permissions.

## Project goal

Practise the Linux file and directory operations used in server administration. This is a filesystem exercise; it does not deploy or run a web application.

## Environment

- Windows host with WSL
- Linux user: mcebisi
- Bash command line

## Completed tasks

| Task | Command | Verified result |
| --- | --- | --- |
| Identify current user | `whoami` | `mcebisi` |
| Check current directory | `pwd` | `/home/mcebisi` |
| Create nested directories | `sudo mkdir -p /app/logs` | Both directories exist |
| Assign ownership for the lab | `sudo chown -R mcebisi:mcebisi /app` | Both directories owned by mcebisi |
| Create configuration file | `touch /app/config.conf` | Empty file created |
| Write a log message | `echo "Started" > /app/logs/server.log` | File contains Started |
| List nested contents | `ls -R /app` | Configuration file and logs directory listed |
| Rename the log | `mv /app/logs/server.log /app/logs/server.bak` | server.bak replaces server.log |
| Inspect permissions | `ls -l /app/config.conf` | `-rw-r--r--` |
| Verify retained contents | `cat /app/logs/server.bak` | Started |

## Final structure

| Path | Purpose |
| --- | --- |
| `/app/config.conf` | Empty configuration placeholder |
| `/app/logs/server.bak` | Renamed log containing `Started` |

## What I learned

- Spaces separate a command from its arguments: `cd ~` works, while `cd~` is interpreted as a command name.
- Absolute paths such as `/app/logs` work regardless of the current directory.
- `mkdir -p` creates missing parent directories.
- `>` redirects output into a file and replaces any existing contents.
- `mv` moves or renames a file. A .bak extension alone does not create a separate backup; `cp` would retain the original.
- `-rw-r--r--` gives the owner read/write access and the group and others read access.
- A successful command often returns to the prompt without printing a message.

## Reproduce the exercise

See [commands.md](commands.md) for the commands and their explanations. Use a disposable lab environment with no existing `/app` directory: the ownership and file-writing commands change files there. Replace `mcebisi` with your Linux username.

## Evidence

The results above were verified from my terminal session. 
## Next learning goals

- Practise copying files with `cp`.
- Explore permissions with `chmod`.
- Read logs using `head`, `tail`, and `less`.

These are future practice goals, separate from the completed checklist.

## Author

Mcebisi Nsele

Learning activity: DecodeLabs DevOps Project 1. This repository contains my own project notes and command record; the training PDF is not redistributed.
ing README.md…]()

