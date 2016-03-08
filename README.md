# install-go
Shell scripts for compiling Go from source or installing and updating Go.  These are consistent with the instructions on https://golang.org/doc/install

These scripts should be run as the user for which you want Go.  __Do not run as `sudo`__.  This breaks things.

## install_current
Installs the current release of Go to `/usr/local/go`.  The `$GOPATH` is set to `~/go` and the directory is created.  `$GOPATH`, `$GOPATH/bin`, and  `/usr/local/go/bin` are added to the `~/.bashrc` file.

## install_go
This script is a copy of [Eric Lagergren's](https://github.com/EricLagergren) [InstallGo](https://gist.github.com/EricLagergren/ddea0f327d38f8c3a918) script.  It allows for more control over the Go install process incuding specifying the `$GOPATH`; installing a specific version of Go; specifying the Go OS and arch; and compiling Go from source.

### License notification for `install_go`

```
version 0.1
By eric@ericlagergren.com

This software is Public Domain.
The person who associated a work with this deed has dedicated
the work to the public domain by waiving all of his or her
rights to the work worldwide under copyright law, including
all related and neighboring rights, to the extent allowed by law.

You can copy, modify, distribute and perform the work, even for
commercial purposes, all without asking permission.

For more information: https://creativecommons.org/publicdomain/zero/1.0/
```

## upgrade_go
Upgrades the currently installed Go to the current version of Go.  All files in `/usr/local/go/`, `$GOPATH/bin/` , and `$GOPATH/pkg/` are removed prior to downloading and installing the current Go.

This script assumes that Go is installed in `/usr/local/go`.


