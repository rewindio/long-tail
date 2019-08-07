# long-tail

Tiny docker container to continuously tail a file

## Intended use

This container is intended to be used with a docker log file collector (like [logspout](https://github.com/gliderlabs/logspout)).  It will allow you to pass in a file on local disk and continually monitor it with output to STDOUT.  Which (for example), logspout will then gather and send to your log aggregation service.

## Example Usage

```bash
docker run -d \
        --name="messages" \
        -v /var/log/messages:/tmp/logfile \
        --privileged \
        rewindio/long-tail
```
