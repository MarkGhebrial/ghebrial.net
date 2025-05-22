+++
template = "page.html"
title = "Setting up postfix"
+++

# Setting up postfix

These are the notes I took when setting up my postfix instance. They are a
reference for my future self, and this page is subject to move or disappear
without notice.

## Useful links:
- [From redhat](https://docs.redhat.com/en/documentation/red_hat_enterprise_linux/8/html/deploying_different_types_of_servers/assembly_mail-transport-agent_deploying-different-types-of-servers)
- Official configuration reference: [www.postfix.org/BASIC_CONFIGURATION_README.html](https://www.postfix.org/BASIC_CONFIGURATION_README.html)

## Installation
```bash
paru postfix
```

## Administration

### Start
```bash
sudo postfix start
```

## Configuration

### Configuration file path
```
/etc/postfix/main.cf
```

After changing the configuration, you must run
```bash
postfix reload
```

### Set domain name
```
mydomain = ghebrial.net
```
