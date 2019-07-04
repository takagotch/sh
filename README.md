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

```py
from sh import ifconfig
print ifconfig("eth0")
```

```sh
pip install sh
pip install -r requirements-dev.txt
python sh.py test
python sh.py test FunctionalTests.test_unicode_arg
python sh.py test -e 3.4 FunctionalTests.test_unicode_arg
python sh.py test
coverage report
coverage html
```
