# Intelligent SOC: Integrated Threat Detection & Response System

B.Sc. graduation project, Faculty of Computers and Artificial Intelligence, Fayoum University (2025-2026).

An integrated SOC platform combining:

- **Infrastructure layer:** Suricata NIDS and a Cowrie SSH/Telnet honeypot
- **Core SIEM layer:** Wazuh Manager for log aggregation and correlation
- **Adaptive intelligence layer:** FastAPI traffic router, XGBoost anomaly detection, and generative AI threat explanation
- **Response automation layer:** SOAR containment workflows

Custom detections are mapped to MITRE ATT&CK (e.g. T1110 SSH brute force, T1498 DoS, T1486 ransomware, T1505.003 web shells).

## Repository layout

| Path | Description |
|------|-------------|
| `wazuh/rules/local_rules.xml` | Custom Wazuh detection rules (SSH brute force, root login, Windows logon failures, sudo, web shells, and more) |
| `wazuh/config/ossec.conf` | Wazuh manager configuration (sensitive values redacted) |
| `docs/` | Full project report (PDF) |

## Notes

- Values such as the admin public IP, Tailscale IPs and the Shuffle webhook ID are replaced with placeholders. Fill in your own before deploying.
- Rules were validated against Wazuh 4.14.5.

## Team

Elsayed El-Khouly (Leader), Mahmoud Saad, Youssef Thabet, Tarek Ziad, Ahmed Hassan

Supervised by Dr. Esraa Rslan; co-supervised by Eng. Ahmed Gomaa Soufi.
