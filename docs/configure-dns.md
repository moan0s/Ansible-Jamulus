# Configuring your DNS server

To set up Jamulus on your domain (e.g. example.com), you'd need to do some DNS configuration.


## DNS settings

| Type | Target                        |
|------|-------------------------------|
| A    | `jamulus-server-IPv4 address` |
| AAAA | `jamulus-server-IPv6 address` |

Be mindful as to how long it will take for the DNS records to propagate.

When you're done configuring DNS, proceed to [Configuring the playbook](configuring-playbook.md).
