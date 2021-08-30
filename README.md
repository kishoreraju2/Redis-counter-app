

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
