# BUMP

> Remotely executable bash script to bump semantic version

Usage

```sh
version=$(git describe --tags --abbrev=0)
curl -sL https://raw.githubusercontent.com/expelledboy/bump/bump.sh | bash -s -- $version minor
```
