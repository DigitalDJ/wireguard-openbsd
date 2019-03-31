# wireguard-openbsd
WireGuard ports for OpenBSD

Place `net/wireguard-tools` and `net/wireguard-go` in your ports tree (usually `/usr/ports`) then:

```shell
cd /usr/ports/net/wireguard-tools
make install
```

`wireguard-tools` depends on `wireguard-go`, therefore both packages will be built and installed.

`wireguard-tools` contains an `rc.d` script that supports a single instance of WireGuard. The `rc.d` script allows checking the run status of the daemon and allows reloading the configuration at runtime. See the [`wireguard-tools README`](net/wireguard-tools/pkg/README) on how to use the `rc.d` script.
