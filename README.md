# go-ip

[![goreport](https://www.goreportcard.com/badge/github.com/nine-monsters/go-ip)](https://www.goreportcard.com/report/github.com/nine-monsters/go-ip)

ip tools

## Usage

```go
import "github.com/nine-monsters/go-ip/pkg/goip"
// ListAllIPv4 list all IPv4 addresses.
// The input argument ifaceNames are used to specified interface names
// (filename wild match pattern supported also, like eth*)
allIPv4s, _ := ip.ListAllIPv4()
allEth0IPv4s, _ := ip.ListAllIPv4("en0")
allEth0En0IPv4s, _ := ip.ListAllIPv4("eth0", "en0")
allEnIPv4s, _ := ip.ListAllIPv4("en*")
// GetOutboundIP  gets preferred outbound ip of this machine.
outboundIP := ip.Outbound()
// MainIP tries to get the main IP address and the IP addresses.
mainIP, ipList := ip.MainIP()
```
