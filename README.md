### sh
---
.go
https://github.com/mvdan/sh

.py
https://github.com/amoffat/sh

http://amoffat.github.io/sh/

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

sh.ls("-l", "/tmp", color="never")

try:
  sh.ls("/doent/exist")
except sh.ErroreturnCode_2:
  print("directory doesn't exist")

sh.ls(_out="/tmp/dir_contents")

with open("/tmp/dir_contents", "w") as h:
  sh.ls(_out=h)
from io import StringIO
buf = String()
sh.ls(_out=buf)

my_ls = sh.ls.bake("-l")

my_ls("/tmp")
sh.ls("-l", "/tmp")

sh.wc(sh.ls("-l"), "-l")

sh.git("show", "HEAD")
sh.git.show("HEAD")

p = sh.find("-name", "sh.py", _bg=True)
p.wait()

from sh import ifconfig
print(ifconfig("wlan0"))

from sh import tar
tar("cvf", "/tmp/test.tar", "/my/home/directory")

from sh import tar
tar("cvf /tmp/test/tar /my/home/directory")

curl("http://duckduckgo.com/", o="page.html", silent=True)
curl("http://duckduckgo.com/", "-o", "page.html", "--silent")
adduser("amoffat", system=True, shell="/bin/bash", no_create_home=True)
adduser("amoffat", "--system", "--shell", "/bin/bash", "--no-create-home")

output = ls("/")
print(output.exit_code)

try:
  print(ls("/some/non-existant/folder"))
except ErrorReturnCode_2:
  print("folder doesn't exist!")
  create_the_folder()
except ErrorReturnCode:
  print("unknown error")

try:
  p = sh.sleep(3, _bg=True)
  p.kill()
except sh.SignalException_SIGKILL:
  print("killed")
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
