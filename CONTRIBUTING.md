# Contributing

## Build and deploy

```bash
rockcraft pack -v
sudo skopeo --insecure-policy copy oci-archive:oathkeeper_0.40.3_amd64.rock docker-daemon:oathkeeper:0.40.3
docker run oathkeeper:0.40.3
```
