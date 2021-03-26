## Remote Write Adapter Example

forked from: https://github.com/prometheus/prometheus/blob/43acd0e2e93f9f70c49b2267efa0124f1e759e86/documentation/examples/remote_storage/example_write_adapter/server.go

This is a simple example of how to write a server to
receive samples from the remote storage output.

To use it:

```
GO111MODULE=on go get github.com/prometheus/prometheus@43acd0e2e93f9f70c49b2267efa0124f1e759e86
go build
./remote_write
```

...and then add the following to your `prometheus.yml`:

```yaml
remote_write:
  - url: "http://localhost:1234/receive"
```

Then start Prometheus:

```
./prometheus
```
