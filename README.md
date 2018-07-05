# Docker Nginx, Fluentd, Elasticsearch

docker-compose to run Nginx and send log to Elasticsearch using Fluentd

## Instruction
- `docker-compose up`

# Notes
- Elasticsearch has only 1 node, so health status will be yellow.
- Kibana is used as-it-is only to check the data is coming, it has no default indices, to see the logs, set indices to `nginx-*`
- Depends on the architecture and application, mounting `/var/log/nginx/` in `Nginx` to host and set `td-agent` config as `@type tail` to the file in host could have less overhead, and not requiring application to send logs to stdout.