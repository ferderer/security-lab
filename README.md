# security-lab

Practical security hardening — Ansible playbooks, configurations, and reference 
implementations. Companion repository to [ferderer.de/blog](https://ferderer.de/blog).

## Contents (planned!)

### Ansible Playbooks

| Playbook | Description |
|---|---|
| `ansible/wsl-setup.yml` | WSL2 base environment setup |
| `ansible/agent-hardening.yml` | AI agent isolation: unprivileged user, bind mount, nftables, Squid |
| `ansible/vps-hardening.yml` | VPS baseline hardening |

### Spring Security

| Module | Description |
|---|---|
| `spring-security/filter-chain-demo` | Spring Security filter chain reference implementation |

## Related Articles

- [Containing the Blast Radius: Hardening WSL2 for AI Coding Agents](https://ferderer.de/blog/tech/ai-agent-wsl2-hardening)

## Usage

```bash
ansible-playbook ansible/agent-hardening.yml --ask-become-pass
```

All sensitive values (usernames, IPs, domains) are parameterized via `group_vars/all.yml`.
