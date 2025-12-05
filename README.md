# borg4win - BorgBackup for Windows

borg4win is a packaging of BorgBackup for Windows systems. It provides a self-contained Cygwin-based environment with BorgBackup, Python, OpenSSH, and required utilities already included, offering a ready-to-use command-line backup solution for Windows.

## Features

- **Complete BorgBackup implementation**: Full-featured BorgBackup for Windows
- **Deduplication**: Efficient storage by saving only unique data chunks across all backups
- **Compression**: Built-in compression support for space-efficient backups
- **Encryption**: Optional authenticated encryption for secure backups
- **Local and remote repositories**: Support for both local and SSH-based remote backup destinations
- **Incremental backups**: Fast, space-efficient incremental backups
- **Data integrity**: Integrity checking to guarantee data consistency
- **Bundled dependencies**: Includes Python, OpenSSH, and Cygwin runtime
- **Portable**: Unzip and run, no installation or system modifications required
- **Wide compatibility**: Works on Windows Vista and newer

## Requirements

- Windows Vista or later
- No external dependencies required — all components included in the package

## Download

Latest releases of borg4win are available on GitHub:

https://github.com/itefixnet/borg4win/releases

Each release includes:
- The complete borg4win ZIP package (BorgBackup, Python, Cygwin runtime, OpenSSH)
- Release notes and version history

## Basic Usage

1. Unzip the downloaded archive

2. For interactive use, start the borg4win environment:
   ```
   borg4win.cmd
   ```

3. Use BorgBackup commands:
   ```
   borg --help
   borg init --encryption=repokey /path/to/repo
   borg create /path/to/repo::archive1 /path/to/source
   borg list /path/to/repo
   borg extract /path/to/repo::archive1
   ```

4. For batch/scripting use:
   ```
   bin\bash -c '/bin/borg --help'
   ```

   Or develop a bash script to exploit all functionality like environment variables, remote shell, etc.

borg4win is tested successfully with local and remote repositories. You should test and verify that it works for your specific needs.

## Links

- **BorgBackup homepage**: https://www.borgbackup.org/
- **BorgBackup documentation**: https://borgbackup.readthedocs.io/en/stable/

## License

borg4win is licensed under the BSD 2-Clause License. See LICENSE file for details.
