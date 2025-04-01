## SUMMARY

Source: https://www.youtube.com/watch?v=MM9gKmpBOVs

The talk, presented by a certified SANS instructor, focuses on identifying threat actor infrastructure, specifically Russian disinformation operations, using security certificates.

## IDEAS:

- Security certificates verify a website's identity and enable encrypted connections, ensuring data safety.
- Every SSL certificate is unique and made public in security certificate transparency logs.
- Security certificates are a valuable, underused resource for open-source intelligence (OSINT) investigators.
- Revoking a security certificate doesn't alter its public availability in transparency logs.
- Certificates provide a strong attribution signal, linking domains to their owners.
- Multiple domains can be rolled into one certificate using a subject alternative name.
- Shared certificates across domains suggest common ownership and control.
- Investigative journalists linked DC weekly.org to John Dugan through security certificates.
- Dugan's denial contradicted certificate records linking him to multiple disinformation websites.
- Finding hidden infrastructure involves mapping subdomains using security certificates.
- Russian state media operations exposed themselves through subdomain naming conventions.
- Sanctioned Russian media operations rebranded to bypass platform bans.
- Security certificates help identify disguised Russian state media brands.
- Cloudflare hides real IP addresses of websites, complicating investigations.
- Server Name Indication (SNI) helps browsers connect to the correct website on shared servers.
- Investigators can use ZGrab2 to perform TLS handshakes and identify real IP addresses.
- Security certificates help map threat actor infrastructure and identify attribution signals.
- The Prava network is a complex Russian disinformation operation targeting multiple countries.
- Investigators use smart narrowing of IP ranges to find threat actor infrastructure.
- Russian disinformation websites disguise themselves using Cloudflare's infrastructure.
- Investigators need to verify findings to ensure accuracy and attribution.
- Security certificates are essential in identifying and mapping threat actor infrastructure.
- ZGrab2 connects to IP addresses to perform TLS handshakes and identify certificates.
- Investigators use certificate transparency logs for verification and analysis.
- Finding real IP addresses helps attribute content to specific threat actors.
- SSL certificates are an essential tool for OSINT investigations.
- Cloudflare's infrastructure complicates investigations but can be bypassed with smart tools.
- Investigators must balance thoroughness with efficiency in identifying threat actor infrastructure.
- Understanding certificate transparency logs is crucial for mapping threat actor networks.
- Security certificates offer a rich, underutilized resource for OSINT investigations.

## INSIGHTS:

- Security certificates are a crucial, underutilized resource for OSINT investigations into threat actors.
- Shared certificates across domains indicate strong attribution and common ownership, aiding investigations.
- Russian state media operations use rebranding and new domains to bypass platform sanctions.
- Investigators can uncover hidden infrastructure by mapping subdomains through certificate analysis.
- SNI allows browsers to connect to the correct website on servers with multiple domains.
- ZGrab2 and similar tools help identify real IP addresses behind Cloudflare's masking.
- Certificate transparency logs provide valuable insights into threat actor infrastructure.
- Russian disinformation networks use complex infrastructure and rebranding to evade detection.
- Investigators must verify findings through transparency logs to ensure accurate attribution.
- Security certificates offer a rich resource for identifying and mapping threat actor networks.

## QUOTES:

- "Security certificates verify the identity of a website."
- "Security certificates are a hugely underutilized resource for OSINT investigators."
- "Every single security certificate is made public in transparency logs."
- "Security certificates provide a very strong signal for attribution."
- "Investigators can map infrastructure to identify malicious behavior using security certificates."
- "You can't alter what's been put out there in certificate transparency logs."
- "Investigative journalists linked DC weekly.org to John Dugan."
- "Russian state media operations exposed themselves through subdomain naming conventions."
- "Security certificates help identify disguised Russian state media brands."
- "Cloudflare can be very frustrating for investigators."
- "Server Name Indication ensures encrypted connections to the correct domain."
- "ZGrab2 helps identify real IP addresses behind Cloudflare."
- "Certificate transparency logs offer insights into threat actor infrastructure."
- "Russian disinformation networks are complex and well-resourced."
- "Investigators must verify findings for accurate attribution."
- "Security certificates are essential for OSINT investigations."
- "Cloudflare complicates investigations but can be bypassed with smart tools."
- "Security certificates offer a rich resource for identifying threat actor networks."
- "Shared certificates indicate common ownership and control."

## HABITS:

- Regularly verify and analyze security certificates for OSINT investigations.
- Utilize tools like ZGrab2 to identify real IP addresses and threat actor infrastructure.
- Map subdomains through certificate analysis to uncover hidden infrastructure.
- Balance thoroughness with efficiency in threat actor investigations.
- Use certificate transparency logs for verification and analysis.
- Leverage shared certificates to identify common ownership and control.
- Investigate complex disinformation networks using security certificates.
- Continuously update knowledge on tools and techniques for OSINT investigations.
- Verify findings to ensure accurate attribution of threat actor networks.
- Adapt to evolving threat actor tactics and infrastructure.

## FACTS:

- Every SSL certificate is unique and made public in transparency logs.
- Revoking a security certificate doesn't alter its public availability.
- Certificates provide a strong attribution signal, linking domains to owners.
- Cloudflare hides real IP addresses, complicating investigations.
- Server Name Indication helps browsers connect to the correct website.
- Russian disinformation networks target multiple countries with complex operations.
- Investigators use ZGrab2 to perform TLS handshakes and identify certificates.
- Security certificates help map threat actor infrastructure and attribution signals.
- Sanctioned Russian media operations rebrand to bypass platform bans.
- Shared certificates across domains suggest common ownership and control.

## REFERENCES:

- DC weekly.org
- John Mark Dugan
- Falconite Tech
- Cert.sh
- Clear Story News
- SANS Institute
- Protection Group International (PGI)
- Certificate Transparency Logs
- Russian State Media Operations
- Cloudflare
- ZGrab2
- Server Name Indication (SNI)
- Prava Network
- Security Trails
- LinkedIn
- Logal Hosting Provider

## RECOMMENDATIONS:

- Investigate security certificates for strong attribution signals in OSINT investigations.
- Map subdomains through certificate analysis to uncover hidden infrastructure.
- Use shared certificates to identify common ownership and control.
- Verify findings through certificate transparency logs for accurate attribution.
- Leverage ZGrab2 to identify real IP addresses behind Cloudflare's masking.
- Balance thoroughness with efficiency in threat actor investigations.
- Investigate complex disinformation networks using security certificates.
- Regularly update knowledge on tools and techniques for OSINT investigations.
- Adapt to evolving threat actor tactics and infrastructure for effective investigations.
- Use certificate transparency logs as a rich resource for OSINT investigations.
