# BUMP

> Remotely executable bash script to bump semantic version

### Online Usage

```sh
bash <(curl -sL https://git.io/bump.sh) $VERSION patch
````

Can bump major, minor and patch releases.

```sh
version=$(git describe --tags --abbrev=0)

update=$(bash <(curl -sL https://git.io/bump.sh) $version minor)

echo $version
# v1.0.0

echo $update
# v1.1.0

update=$(bash <(curl -sL https://git.io/bump.sh) $version major)

echo $update
# v2.0.0
```

Used [git.io](https://github.blog/2011-11-10-git-io-github-url-shortener/) for url shortener.

### Offline Usage

```sh
mkdir scripts && cd scripts

curl -OL https://git.io/bump.sh
#   % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
#                                  Dload  Upload   Total   Spent    Left  Speed
#   0     0    0     0    0     0      0      0 --:--:--  0:00:01 --:--:--     0
# 100   666  100   666    0     0    290      0  0:00:02  0:00:02 --:--:--  1503

chmod +x bump.sh

version=$(git describe --tags --abbrev=0)

./bump.sh $version patch
# v1.0.1
```
