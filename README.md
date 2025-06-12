# caddy-docker-proxy-cloudflaredns
Barebones rebuild of caddy-docker-proxy with cloudflare dns

First, set up cloudflare to allow for LetsEncrypt; 
[this guide](https://roelofjanelsinga.com/articles/using-caddy-ssl-with-cloudflare/) shows how to set up cloudflare to permit cert generation for your host.

## Installation

### Just do it

1. set your `CLOUDFLARE_API_TOKEN` environment variable
2. run `docker run ghcr.io/cmcconomy/caddy-docker-proxy-cloudflaredns`

### Or, do this at home if you dare

To build, run `docker compose build && docker compose up`.

## Testing it out
try `curl -k --resolve who.mydomain.com:443:127.0.0.1 https://who.mydomain.com`
