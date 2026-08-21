# Lab Architecture

## Network

The laboratory is isolated from the host's personal network.

## Network range

10.10.10.0/24

## Virtual machines

| Host    |      IP     |       Role            |
|---------|-------------|-----------------------|
| WAZUH   | 10.10.10.10 | SIEM / Log collection |
| LINUX01 | 10.10.10.20 | Monitored Linux host  |
| LINUX02 | 10.10.10.30 | Internal Linux server |

## Architecture

```text
                 CTI / Research
                       |
                       v
              TTP / MITRE ATT&CK
                       |
                       v
                Simulated Activity
                       |
              +--------+--------+
              |                 |
           LINUX01           LINUX02
              |                 |
              +--------+--------+
                       |
                     Logs
                       |
                       v
                     WAZUH
                       |
                       v
               Detection / Hunting