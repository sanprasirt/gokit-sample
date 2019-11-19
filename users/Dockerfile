FROM golang

RUN mkdir -p /go/src/github.com/sanprasirt/gokit-sample

ADD . /go/src/github.com/sanprasirt/gokit-sample

RUN go get  -t -v ./...
RUN go get  github.com/canthefason/go-watcher
RUN go install github.com/canthefason/go-watcher/cmd/watcher

ENTRYPOINT  watcher -run github.com/sanprasirt/gokit-sample/users/cmd  -watch github.com/sanprasirt/gokit-sample/users
