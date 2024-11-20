# Testing

1. Build

`docker build -t localfluentd .`

2. Run with both labels activated.

`docker run --rm -e FLUENTD_ELASTICSEARCH="fluent-elasticsearch.conf" -e FLUENTD_OPENSEARCH="fluent-opensearch.conf" localfluentd`

3. Disable @ELASTICSEARCH label where `FLUENTD_ELASTICSEARCH` will point to `fluent-null.conf` which discards the events.

`docker run --rm -e FLUENTD_ELASTICSEARCH="fluent-null.conf" -e FLUENTD_OPENSEARCH="fluent-opensearch.conf" localfluentd`