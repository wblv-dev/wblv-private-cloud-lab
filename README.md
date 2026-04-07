# WBLV Private Cloud Lab

A full SOC lab built from an empty rack. Services generate real telemetry for detection engineering, every bit of day-to-day use feeds the security lifecycle.

**[Documentation →](https://wellbelove.org/wblv-private-cloud-lab/)**

## What This Is

The household gets real services that improve quality of life. I get a technical SOC lab. They co-exist, all secure, all under one roof.

The end goal: write KQL in Microsoft Sentinel against real, enriched data from infrastructure I own and operate.

## What's In This Repo

This repo only stores logic/code, Ansible playbooks, Sentinel analytics rules, IOC reference data. It is not a project tracker or documentation site.

```
ansible/          Inventory, roles, playbooks
sentinel/         Analytics rules, workbooks
ioc/              IOC lists and reference data for KQL
```

Configuration values (IPs, hostnames, secrets) are never committed. They come from Ansible Vault, 1Password, or NetBox at runtime.

## Log Pipeline

```
Source → Event Forwarder → Aggregation (enrich, filter) → Sentinel (hunt, detect, respond)
```

Logging is a build requirement, not a feature. Every service ships logs from day one.

## Links

- [Documentation](https://wellbelove.org/wblv-private-cloud-lab/) — technical reference for the full lab
- [Blog](https://wellbelove.org/blog/) — the journey, decisions, and lessons learned
