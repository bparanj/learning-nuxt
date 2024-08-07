## Versions

### Development - Control Node

| Name      | Version     |
| --------- | ----------- |
| Python    | 3.12.1      |
| Ansible   | core 2.16.1 |
| Node      | v21.6.2     |
| npm       | 10.5.0      |
| AMI       | 0.0.27      |

The AMI image version in ami.yml and provision.yml must be same.

#### Python

```
python3 --version
Python 3.12.1
```

#### Ansible

```
ansible --version
ansible [core 2.16.1]
  config file = None
  configured module search path = ['/Users/bparanj/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
  ansible python module location = /opt/homebrew/Cellar/ansible/9.1.0/libexec/lib/python3.12/site-packages/ansible
  ansible collection location = /Users/bparanj/.ansible/collections:/usr/share/ansible/collections
  executable location = /opt/homebrew/bin/ansible
  python version = 3.12.2 (main, Feb  6 2024, 20:19:44) [Clang 15.0.0 (clang-1500.1.0.2.5)] (/opt/homebrew/Cellar/ansible/9.1.0/libexec/bin/python)
  jinja version = 3.1.3
  libyaml = True
```

### Production - Target Node

| Name         | Version                                                                                  |
| ------------ | ---------------------------------------------------------------------------------------- |
| ruby-install | 0.9.3                                                                                    |
| Ruby         | 3.3.0                                                                                    |
| Gem          | 2.3.6                                                                                    |
| Goss         | 0.4.4                                                                                    |
| Caddy        | 2.7.6                                                                                    |
| PostgreSQL   | psql (PostgreSQL) 16.2 (Ubuntu 16.2-1.pgdg22.04+1)                                       |
| Redis        | Redis server v=7.2.4 sha=00000000:0 malloc=jemalloc-5.3.0 bits=64 build=4a33ab3ec422ece7 |
| Git          | git version 2.34.1                                                                       |

### Testing

#### Goss

See the playbooks/goss.yml:

```
v0.4.4
```

## Base Image

### Caddy

```
caddy version
v2.7.6 h1:w0NymbG2m9PcvKWsrXO6EEkY9Ru4FJK8uQbYcev1p3A=
```

### Postgresql

```
sudo -u postgres psql
SELECT version();
```

```
PostgreSQL 16.2 (Ubuntu 16.2-1.pgdg22.04+1) on x86_64-pc-linux-gnu, compiled by gcc (Ubuntu 11.4.0-1ubuntu1~22.04) 11.4.0, 64-bit
```

### Redis

```
redis-server --version

```
