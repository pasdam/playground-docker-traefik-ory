# playground-docker-traefik-ory

Playground to test [Ory](https://www.ory.sh/) components integration with
[Traefik](https://traefik.io/) in docker.

## Requirements

* docker.

## Services

* [Traefik](https://traefik.io/);
* [Kratos](https://www.ory.sh/kratos/).

## Usage

To start all the services

```bash
docker compose up
```

Then you can reach the web services:

* [traefik dashboard](https://localhost): dashboard where you can see all the
  routes and services configured in Traefik;
* [self service UI](https://localhost/website/): it's a test UI were you can
  perform all operations using kratos (sign up, sign in, ...);
* [mailslurper](http://localhost:4436): it's a UI to view the emails sent by
  kratos.

Note that for services accessed through Traefik you wil receive a warning about
the certificate from the browser, this is due to the fact that we're using self
signed certificates.
