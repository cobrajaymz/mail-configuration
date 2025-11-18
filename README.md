# Bibans Mail Server Configuration

This repository contains the configuration files used to deploy a simple mail server for the domain **bibans.mail**.

## Contents

- **named.conf.local**  
  DNS zone declaration for `bibans.mail`.

- **bibans.mail.db**  
  DNS zone file with A and MX records.

- **main.cf**  
  Postfix main configuration file.

- **master.cf**  
  Postfix service configuration.

## Purpose

These files are used for a local test environment where:
- BIND9 provides DNS resolution
- Postfix handles email delivery
- Tailscale IPs are used for host communication

## How to Use

1. Place the DNS files inside `/etc/bind/`.
2. Reload BIND:
3. sudo systemctl reload bind9
4. Place Postfix files in `/etc/postfix/`.
5. Restart Postfix with: sudo systemctl restart postfix

