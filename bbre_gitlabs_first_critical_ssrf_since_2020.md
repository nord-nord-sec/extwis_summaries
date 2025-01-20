# SUMMARY

Johan Carlsson discusses exploiting an SSRF vulnerability in GitLab's analytic dashboards, demonstrating its critical impact and payout.

Source: https://www.youtube.com/watch?v=YQ5ixykKnyY

# IDEAS

- SSRF vulnerability exploited in GitLab's analytic dashboards led to critical security impact.
- Bug was discovered in a new functionality called analytic dashboards.
- Configuration involved setting a URL as a third-party website.
- Multiple URLs within a Kubernetes cluster were vulnerable to SSRF.
- Only one URL allowed full read, returning errors and payloads.
- Impact demonstrated by accessing internal and production infrastructure.
- Past critical SSRF in Grafana hardened GitLab's infrastructure.
- Severity rated similarly for both GitLab.com and self-hosted instances.
- GitLab's local or Docker installation exposes multiple services.
- Redis exporter in GitLab can leak keys and values from Redis.
- Redis exporter works with Unix sockets, not just IP addresses.
- GitLab runner tokens stored in Redis could be exploited.
- Runner tokens enable impersonation and execution of jobs.
- Exploiting runner tokens can lead to remote code execution.
- Discovering the vulnerability required extensive testing and code review.
- Allow local requests flag in HTTP requests led to SSRF discovery.
- Vulnerability allowed regular users to configure malicious URLs.
- GitLab's self-registration policy impacted vulnerability severity rating.
- SSRF exploited through GitLab's runner registration process.
- GitLab warned about runner token secrecy in documentation.
- Redis logs monitored to identify sensitive information leakage.
- Exploitation complexity involved matching IPs with CSRF tokens.
- GitLab's scope policy treated SSRF vulnerabilities with specific edge cases.
- Runner tokens could potentially access sensitive source code.
- Exploit demonstrated the importance of thorough code review.
- Previous SSRF incidents informed GitLab's security measures.
- Redis's low-level TCP language used in SSRF exploitation.
- GitLab's runner jobs can access, build, and deploy code.
- Redis exporter provides metadata and statistics for Prometheus.
- GitLab's SSRF vulnerability highlighted the need for robust security.
- SSRF vulnerability exploitation required no privilege escalation.

# INSIGHTS

- SSRF vulnerabilities can lead to critical security impacts if not mitigated.
- Thorough code review is essential for identifying potential security flaws.
- Runner tokens can be highly sensitive and require stringent protection.
- Redis's low-level language can be exploited for malicious purposes.
- GitLab's infrastructure requires constant monitoring and hardening.
- SSRF vulnerabilities can escalate to remote code execution.
- Security measures must consider both internal and external threats.
- Regular users can exploit vulnerabilities if security is not robust.
- Documentation should emphasize the importance of token secrecy.
- Monitoring logs is crucial for detecting sensitive data leaks.

# QUOTES

- "It’s not the typical full read SSRF where you just read the metadata."
- "Bug was in a fairly new functionality, they called it analytic dashboards."
- "You configure this as an administrator on the platform."
- "All of these were in different ways, suspect to SSRF."
- "You could actually get the error back."
- "They just sent you back whatever the JSON parsing did."
- "I could get a full read both on my internal or like my self-hosted instance."
- "They have hardened it quite a lot since then."
- "You can get the highest bounty, both for the self-hosted and the com one."
- "I started to look at different services that are running inside GitLab."
- "I could point to this Redis instance and get keys and values back."
- "Redis exporter has a path that is called slash scrape."
- "You can give it a URL as a query parameter."
- "Redis exporter also could work with Unix sockets."
- "You can search for different keys in the Redis instance."
- "They say this token is supposed to be secret."
- "In the context of GitLab, these are running on separate servers called the runners."
- "Runner authenticates using the token."
- "You could get a list of all the runner tokens on the instance."
- "This creates in the end, RCE in all of the runner jobs on GitLab."
- "I also tried to read all of the old SSRF reports I could find from GitLab."
- "They always treat if you need an account, it will be low."
- "Exploiting this more, I just thought about different things and tested out."
- "They had put in the flag, allow local requests."
- "This is the best thing."

# HABITS

- Regular code review helps identify potential security vulnerabilities.
- Monitoring logs provides insights into potential data leaks.
- Testing different features to discover sensitive information.
- Maintaining awareness of previous security incidents for better protection.
- Using documentation to understand potential vulnerabilities.
- Exploring various exploitation methods for comprehensive security analysis.
- Utilizing safe wrappers for HTTP requests to prevent SSRF.
- Keeping tokens and sensitive information secret.
- Analyzing infrastructure to identify potential security threats.
- Continuously thinking about new ways to exploit vulnerabilities.
- Leveraging existing reports for insights into vulnerability management.
- Understanding flag settings in code for potential security implications.
- Analyzing the impact of self-registration policies on security severity.
- Reviewing documentation for warnings about sensitive information.
- Investigating runner registration processes for potential vulnerabilities.

# FACTS

- SSRF vulnerabilities can allow unauthorized access to internal systems.
- GitLab's analytic dashboards were vulnerable to SSRF exploitation.
- Redis exporter can leak keys and values from Redis instances.
- Unix sockets can be exploited in SSRF attacks.
- GitLab runner tokens are stored in Redis and can be exploited.
- Runner tokens allow impersonation and execution of jobs.
- Allow local requests flag can lead to SSRF vulnerabilities.
- GitLab warns about the secrecy of runner tokens in documentation.
- SSRF vulnerabilities can escalate to remote code execution.
- Redis's low-level language can be used for malicious purposes.
- GitLab's infrastructure requires constant monitoring and hardening.
- Monitoring logs is crucial for detecting sensitive data leaks.
- GitLab's scope policy treats SSRF vulnerabilities with specific edge cases.
- Redis exporter provides metadata and statistics for Prometheus.
- SSRF vulnerability exploitation required no privilege escalation.

# REFERENCES

- GitLab
- Kubernetes
- Docker
- Grafana
- Prometheus
- Redis
- Redis exporter
- JSON
- CSRF tokens
- GitLab runner

# RECOMMENDATIONS

- Conduct thorough code reviews to identify potential security vulnerabilities.
- Regularly monitor logs for signs of sensitive data leaks.
- Test different features to uncover sensitive information.
- Maintain awareness of past security incidents for improved protection.
- Use documentation to understand potential vulnerabilities.
- Explore various exploitation methods for comprehensive security analysis.
- Utilize safe wrappers for HTTP requests to prevent SSRF.
- Keep tokens and sensitive information secret.
- Analyze infrastructure to identify potential security threats.
- Continuously think about new ways to exploit vulnerabilities.
- Leverage existing reports for insights into vulnerability management.
- Understand flag settings in code for potential security implications.
- Analyze the impact of self-registration policies on security severity.
- Review documentation for warnings about sensitive information.
- Investigate runner registration processes for potential vulnerabilities.
