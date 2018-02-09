### [GOROOT to Ubuntu](https://golang.org/doc/install)
### [GOPATH GOBIN to Ubuntu](https://github.com/golang/go/wiki/SettingGOPATH)

* Open ``` sudo vim $HOME/.profile ``` File and Add Following Four Lines
```sh
export GOROOT=/opt/go
export PATH=$PATH:$GOROOT/bin
export GOPATH=$HOME/data/code/golang
export GOBIN=$HOME/data/code/golang/bin
```

### Check GOPATH Added
```sh
go env GOPATH
```

### Important Notes
```
Leave GOROOT alone. 
It should either be unset, or set to the installation folder.

On the other hand, the GOPATH should *not* point to the Go installation, 
but rather to your workspace (see https://golang.org/doc/code.html#GOPATH). 
Whenever you install some package with go get or go install, 
it will land within the GOPATH. That is why it warns you, 
that you most definitely do *not* want random packages 
from the internet to be dumped into your official installation.
Create one or more folders where you'd like to develop 
Go code and set those as your GOPATH (note, if multiple are set, 
then go get will pull and install packages into the first).


GOROOT is seto to /usr/local/go by default.
That value is burnt into the binary you downloaded.

GOPATH to a path that you own. I suggest export GOPATH=$HOME, 
although this is highly subject to personal taste.

Please read http://golang.org/doc/code.html for more information.
```