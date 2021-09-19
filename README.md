# BUMP

> Remotely executable bash script to bump semantic version

Usage

```sh
export version=$(git describe --tags --abbrev=0)
bash <(curl -sL https://git.io/bump.sh) $version minor
```

Used (git.io)[https://github.blog/2011-11-10-git-io-github-url-shortener/] for url shortener.
