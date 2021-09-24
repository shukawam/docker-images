# Squid

A forward proxy that simply works.

## Install & How to Use

clone this repository.

```bash
git clone https://github.com/shukawam/docker-images.git
cd squid
```

Then, modify `etc/squid/squid.conf` and `etc/squid/squid-log.conf` with your environment.

```conf
acl localnet src <your-host>/32
```

build and run.

```bash
docker-compose up -d
```
