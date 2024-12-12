# Privilege Escalation
This is quite related to my previous work as reseacher, and this section currently just focus on Windows OS environment. :))) I will update the others when I learn them

## What is this
- This tactic is one of the most important steps in a cyber attack. 
- This involves exploiting system vulnerabilities, misconfigurations, or weaknesses in user permissions 
- Upon success, attacker can move from a lower privilege level (e.g., a standard user) to a higher one (e.g., administrator or root access)

## Attack Vector

After cover most techniques from Mitre, I come up with some popular attack vectors

- Misconfig
    - Based on the configuration unsafe like registry, services, permissions,...
- Kernel Driver
    - Target to drivers, libraries that run in kernel mode. These binary can be exploited (0-day CVE) to escalate to higher privilege
    - But this is regurlarly patched by Microsoft pretty fast
- Weak Service
    - Attack to services like web server IIS, databases, ...

## References
