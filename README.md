# HighRiskASNs

High-risk IP and ASN lists based on bot traffic ratio and abuse score.

## Files

| File | Description |
|------|-------------|
| `high_risk_ips.csv` | IP/CIDR networks with bot ratio >= 40% or abuse score > 0 |
| `high_risk_asn.csv` | ASN aggregated list with the same criteria |

## Fields

### high_risk_ips.csv

| Field | Description |
|-------|-------------|
| network | IP/CIDR range |
| asn | Autonomous System Number |
| asn_name | ASN name |
| country | Country code |
| hosting | Hosting provider flag (0/1) |
| abuse | Abuse score |
| bot | Bot traffic ratio (%) |

### high_risk_asn.csv

| Field | Description |
|-------|-------------|
| asn | Autonomous System Number |
| asn_name | ASN name |
| country | Country codes (comma-separated) |
| max_bot | Maximum bot traffic ratio (%) |
| max_abuse | Maximum abuse score |
| network_count | Number of networks matching criteria |

## Criteria

- Bot traffic ratio >= 40%, OR
- Abuse score > 0

Sorted by bot traffic ratio (descending).

## Data Source

- Bot traffic ratio: [Cloudflare Radar](https://radar.cloudflare.com/)

## Update

Updated irregularly.

## License

This data is licensed under [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/).

Bot traffic data sourced from Cloudflare Radar under CC BY-NC 4.0.
