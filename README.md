# Zerodha Ops Task

## Description

This is a sample `Go` application which connects to Redis. The app increments a Redis `counter` on an incoming request.

### Setting up the app

- Use `make build` to compile the binary.
- Set the environment variables:
  - `DEMO_APP_ADDR`: Address where the app should listen to
  - `DEMO_REDIS_ADDR`: Address where Redis is running

## Tasks

- Create a `Dockerfile` for the app.

- Create a `docker-compose.yml` for the app which includes the following:

  - `redis` service, with the data directory of `redis` mounted at `/data` in your VM.
  - `app` service running with port `8000` exposed to the host.

- Launch an Ubuntu server.

- Use Ansible playbook to configure the following:

  - Setup hostname of VM as `demo-ops`.
  - Create a user `demo`.
  - Configure `sysctl` for sane defaults. For eg: increasing open files limit. Configure a variety of `sysctl` settings to make the VM a production grade one.
  - Set the system's timezone to "Asia/Kolkata".
  - Install Docker and Docker-Compose.
  - Deploy the `docker-compose.yml` in `/etc/demo-ops` and start the services.

- Commit the scripts to Github and share the link.

# Requirements

- Ansible
- Vagrant
- Virtual box



# Sysctl config
- Sysctl config for redis (https://redis.io/topics/admin)
  - Setup some swap 
  - overcommit_memory to be 1
  - maxconn to 1024

- Sysctl config for security
  Recommended from https://www.cyberciti.biz/faq/linux-kernel-etcsysctl-conf-security-hardening/

# Test
```
git clone https://github.com/kishoreraju2/Redis-counter-app.git
cd Redis-counter-app
vagrant up
```
