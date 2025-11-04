# Cheatsheet for Shell Commands

---

## Basic Shell Navigation

| Command                     | Name                    | Description                                                              |
| --------------------------- | ----------------------- | ------------------------------------------------------------------------ |
| `ls`                        | List contents           | Lists files and directories in the current location                      |
| `pwd`                       | Print working directory | Outputs the absolute path of the current folder                          |
| `cd <dir>`                  | Change directory        | Switches to `<dir>`; use `cd ..` to move up one level                    |
| `mkdir <dir>`               | Make directory          | Creates a new directory named `<dir>`                                    |
| `touch <file>`              | Create/update file      | Creates an empty `<file>` or updates its modified timestamp              |
| `mv <src> <dest>`           | Move or rename          | Moves `<src>` to `<dest>` or renames it if the destination is a new name |
| `cp <src> <dest>`           | Copy file               | Copies `<src>` to `<dest>`                                               |
| `rm <file>`                 | Remove file             | Deletes `<file>` permanently                                             |
| `cat <file>`                | Concatenate             | Displays the contents of `<file>` or multiple files in sequence          |
| `history`                   | Command history         | Lists recently executed commands                                         |
| `clear`                     | Clear screen            | Clears the terminal display buffer                                       |
| `tab`                       | Autocomplete key        | Pressing the Tab key auto-completes commands and file names              |
| `whoami`                    | Current user            | Outputs the effective user name                                          |
| `USER`                      | Environment variable    | Holds the name of the current user                                       |
| `HOME`                      | Environment variable    | Stores the absolute path to the user's home directory                    |
| `PATH`                      | Environment variable    | Colon-delimited list of directories searched for executables             |
| `PS1`                       | Prompt variable         | Controls the appearance of the interactive shell prompt                  |
| `man <command>`             | Manual pages            | Displays documentation for `<command>`                                   |
| `which <command>`           | Locate executable       | Prints the path of the executable run for `<command>`                    |

---

## Common Options and Variations

| Command                     | Name                    | Description                                                              |
| --------------------------- | ----------------------- | ------------------------------------------------------------------------ |
| `ls -a`                     | List all                | Includes hidden entries whose names start with `.`                       |
| `ls -t`                     | Sort by time            | Orders output by most recently modified first                            |
| `ls -l`                     | Long listing            | Shows detailed metadata such as permissions and size                     |
| `ls -alt`                   | Combined listing        | Runs `ls -a -l -t`: all entries, long format, sorted by time             |
| `cd -`                      | Previous directory      | Jumps back to the last directory you were in                             |
| `mkdir -p <path>`           | Nested directories      | Creates `<path>`, including any missing parent folders                   |
| `cp -r <src> <dest>`        | Recursive copy          | Copies directories and their contents recursively                        |
| `ln -s <target> <link>`     | Symbolic link           | Creates `<link>` that points to `<target>`                               |
| `rm -r <dir>`               | Recursive remove        | Removes `<dir>` and everything inside it                                 |
| `rm -f <path>`              | Force remove            | Suppresses prompts and ignores missing files while deleting              |
| `find . -name "*.txt"`      | Find by name            | Recursively locates files matching the pattern                           |
| `z*`                        | Wildcard match          | Globs files whose names begin with `z`                                   |

---

## Editing Text

| Command                     | Name                    | Description                                                              |
| --------------------------- | ----------------------- | ------------------------------------------------------------------------ |
| `less <file>`               | Pager                   | Opens `<file>` for scrolling with navigation keys                        |
| `sort <file>`               | Sort lines              | Outputs `<file>` with lines ordered alphabetically                       |
| `uniq <file>`               | Unique adjacent lines   | Collapses consecutive duplicate lines from sorted input                  |
| `grep "pattern" file`       | Pattern search          | Shows lines in `file` that match `"pattern"`                             |
| `sed 's/old/new/' file`     | Substitute first match  | Replaces the first occurrence of `old` with `new` on each line           |
| `head -n 10 <file>`         | First lines             | Shows the first 10 lines of `<file>`                                     |
| `tail -n 10 <file>`         | Last lines              | Shows the last 10 lines of `<file>`                                      |
| `tail -f <file>`            | Follow file             | Streams appended lines of `<file>` in real time                          |
| `wc -l <file>`              | Line count              | Counts the number of lines in `<file>`                                   |
| `grep -i "pattern" file`    | Case-insensitive grep   | Matches `"pattern"` without regard to letter case                        |
| `grep -R "pattern" dir`     | Recursive grep          | Searches every file under `dir` for `"pattern"`                          |
| `grep -Rl "pattern" dir`    | Recursive grep (list)   | Outputs only filenames containing `"pattern"`                            |
| `sed -i 's/old/new/g' file` | In-place substitution   | Applies the replacement globally and saves the result to the file        |
| `awk '{print $1}' file`     | Field extractor         | Prints the first whitespace-separated field from each line               |
| `cut -d, -f2 file.csv`      | Column extract          | Prints the second comma-separated field from `file.csv`                  |
| `nano file`                 | Nano text editor        | Opens the nano editor on `file`                                          |
| `vim file`                  | Vim text editor         | Opens the Vim editor on `file`                                           |

---

## Shell Functions

| Command                     | Name                    | Description                                                              |
| --------------------------- | ----------------------- | ------------------------------------------------------------------------ |
| `xargs command`             | Build arguments         | Converts input lines into arguments for `command`                        |
| `command > file`            | Redirect output         | Overwrites `file` with standard output from `command`                    |
| `command >> file`           | Append output           | Appends standard output from `command` to `file`                         |
| `command < file`            | Redirect input          | Uses `file` as standard input for `command`                              |
| `cmd1 \| cmd2`              | Pipe                    | Sends `cmd1`'s standard output into `cmd2`'s standard input              |
| `tee file`                  | Split output            | Writes output to `file` while also printing to the terminal              |
| `echo "Hello"`              | Echo literal            | Prints the quoted string to standard output                              |
| `alias name="command"`      | Alias                   | Assigns a shortcut name to substitute the specified command              |
| `alias pd="pwd"`            | Alias example           | Creates `pd` as a short form of `pwd`                                    |
| `source ~/.shell_profile`   | Reload profile          | Applies changes to the shell profile without restarting the shell        |
| `~/.shell_profile`          | Shell profile           | Startup script that configures your shell environment                    |
| `echo $HOME`                | Echo variable           | Prints the value of the `HOME` environment variable                      |
| `echo $PATH`                | Echo variable           | Shows the colon-delimited list of executable search paths                |
| `export VARIABLE="value"`   | Export variable         | Makes `VARIABLE` available to the current shell and child processes      |
| `unset VARIABLE`            | Unset variable          | Removes `VARIABLE` from the environment                                  |
| `env`                       | Show environment        | Displays all current environment variables and their values              |
| `~`                         | Home shortcut           | Represents the current user's home directory                             |
| `~/project`                 | Home path prefix        | Short form for a path inside the home directory                          |

---

## System Information and Management

| Command                     | Name                    | Description                                                              |
| --------------------------- | ----------------------- | ------------------------------------------------------------------------ |
| `chmod +x script.sh`        | Change mode             | Grants execute permission to `script.sh`                                 |
| `chown user:group file`     | Change owner            | Sets the owner and group for `file`                                      |
| `df -h`                     | Disk usage (filesystem) | Shows mounted filesystem space in human-readable units                   |
| `du -sh <dir>`              | Disk usage (dir)        | Reports the size of `<dir>` with a human-readable total                  |
| `ps aux`                    | Process status          | Lists running processes with details                                     |
| `top`                       | Process monitor         | Displays live CPU and memory usage by process                            |
| `kill <pid>`                | Terminate process       | Sends SIGTERM to the process identified by `<pid>`                       |
| `kill -9 <pid>`             | Force kill              | Sends SIGKILL to stop `<pid>` immediately                                |
| `date`                      | Current date/time       | Prints the system date and time                                          |
| `uptime`                    | System uptime           | Shows how long the system has been running                               |
| `ssh user@host`             | Secure shell            | Opens a remote shell session using SSH                                   |
| `scp <src> <dest>`          | Secure copy             | Transfers files between hosts over SSH                                   |

---

## Networking and Compression

| Command                     | Name                    | Description                                                              |
| --------------------------- | ----------------------- | ------------------------------------------------------------------------ |
| `curl https://example.com`  | Transfer data           | Fetches content from a URL over HTTP/HTTPS                               |
| `tar -czf archive.tgz dir`  | Create tarball          | Compresses `dir` into a gzipped tar archive                              |
| `zip archive.zip file`      | Zip archive             | Compresses `file` (or files) into `archive.zip`                          |
| `unzip archive.zip`         | Extract zip             | Unpacks the contents of `archive.zip`                                    |
| `tar -xzf archive.tgz`      | Extract tarball         | Decompresses and extracts `archive.tgz`                                  |

---
*This cheatsheet provides a quick reference to commonly used shell commands and their options. For more detailed information, refer to the manual pages using the `man` command.*
