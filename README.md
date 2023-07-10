# PkgBox

PkgBox, or Package Box if you will, is a *very very very early stage tool* to manage
rpm builds, build roots and repositories in containers.

It relies on podman-remote to manage "build boxes" which are containers.

It uses a "dumb" method of communication between the client CLI and build boxes by invoking a "rpc" CLi
inside those containers which uses [json rpc 2.0][https://www.jsonrpc.org/specification] as payload.

The base builder image needs to be built before using the CLI which is located at `images/builder-base`.

The "RPC CLI" is located at `images/builder-base/files/opt/pkgbox/pkgbox-rpc`.

## Dependencies

You should be able to run it on Fedora without a python virtual environment by installing:

* podman
* python3-podman
* python3-click

## License

[MIT](./LICENSE)
