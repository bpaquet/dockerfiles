FROM alpine:3.8

RUN apk add --no-cache --update ca-certificates

RUN apk add --no-cache --update --virtual .deps go git musl-dev \
  && go get -d github.com/kubernetes-incubator/external-storage || true \
  && cd /root/go/src/github.com/kubernetes-incubator/external-storage/snapshot \
  && git checkout c463bd186f4cc7abe1e042e050b34563fd4b4f2d \
  && go build -o /snapshot-controller cmd/snapshot-controller/snapshot-controller.go \
  && go build -o /snapshot-pv-provisioner  cmd/snapshot-pv-provisioner/snapshot-pv-provisioner.go \
  && apk del .deps \
  && rm -rf /usr/share/man /tmp/* /var/cache/apk/* /root/go /root/.cache  
