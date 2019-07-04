### sh
---
.go
https://github.com/mvdan/sh

.py
https://github.com/amoffat/sh

.js

.java

```sh
cd $(mktemp -d); go mod init tmp; go get mvdan.cc/sh/cmd/shfmt
cd $(mktemp -d); go mod init tmp; go get mvdan.cc/sh/v3/cmd/shfmt
shfmt -l -w script.sh
shfmt -d .
echo '${foo:1 2}' | bash -n
echo '${foo:1 2}' | shfmt
echo 'foo=(1 2)' | bash --posix -n
echo 'foo=(1 2)' | shfmt -p
cd $(mktemp -d); go mod init tmp; go get mvdan.cc/sh/v3/cmd/gosh
git checkout fuzz
./fuzz
echo '${array[spaced string]}' | shfmt
echo '${array[dash-string]}' | shfmt
{array[dash - string]}
echo '$((foo); (bar))' | shfmt
docker build -t my:tag -f cmd/shfmt/Dockerfile .
```

```sh


```

```
```
