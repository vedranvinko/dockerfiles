# nginx

Expose your public IP addr

- build like `docker build -t nginx .`
- run like `docker run --name some-nginx -p 8080:80 -d nginx`
- put it into your `curl` and smoke it `curl -s localhost:8080/ip` or `curl -s localhost:8080/json_ip`
- bonus points for piping that to `jq` - `curl -s localhost:8080/json_ip | jq`
