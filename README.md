# china-app-domains

GL.iNet / OpenWrt VPN bypass lists for Chinese domestic services.

## Files

| File | Format | Use case |
|------|--------|----------|
| `openwrt-domains` | One domain per line | GL.iNet VPN Policy → Domain/IP → Import from URL |
| `openwrt-ipv4` | One CIDR per line | GL.iNet VPN Policy → Domain/IP → Import from URL |
| `edu-cn-ipv4` | One CIDR per line | China Education Network (CERNET) IPs only |

## GL.iNet MT5000 / MT3000 setup

1. **VPN** → **VPN Dashboard** → select your VPN tunnel
2. **Proxy Mode** → **Customize Routing Rules**
3. **Domain / IP** tab → tick **Do not use VPN for the following**
4. **Add** → **Import from URL** → paste the raw URL below

### Raw URLs

```
https://raw.githubusercontent.com/<your-username>/china-app-domains/main/openwrt-domains
https://raw.githubusercontent.com/<your-username>/china-app-domains/main/openwrt-ipv4
```

## Format

Plain text, one entry per line. Lines starting with `#` are comments (GL.iNet ignores them).

- **Domains** — suffix-matched, so `qq.com` covers `v.qq.com`, `mp.weixin.qq.com`, etc.
- **CIDRs** — standard IPv4 CIDR notation, e.g. `47.52.0.0/16`

## Sources

Curated manually + cross-referenced with public ASN data.
IP ranges sourced from published ASN allocations for each company.
