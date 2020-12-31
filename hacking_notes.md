hacker101.com
pentester labs

read bugbounty blog post how they found bugs

LinEnum.sh
linuxprivchecker.py 

# Skills good to have
1. Cloud skills how to spin up a VM / VPS on AWS, azure
    - nmap scan with a huge ip list can take hours however if you give 5 ips to 20-30 droplets on digitalOcean might take an hour or so.
2. Understanding impact!
    - Information disclosure, depends on impact, PII can cause an impact. AWS private keys (super impactful)
    - Email address is not that impactful (depends)
    - What is relivant for the company
3. OWASP top 10 list know them


# Bug bounty automation
1. Store your data somewhere! psql, mysql, any DB must be organized and easily searchable
2. What to store? Ips, port numbers, DNS, sub-domains, https response, html titles, http status codes
    - More the better however more space is used
3. How to handle alerting? slack notifications, push output to txt file and watch it.
4. Notification fatigue, use batch Notifications every morning at 8am?
    - Example only send notification about sub-domains discovered last 24 hours
5. Create seperate channel for recon, and actual Vulnerability results.

## Up and running
1. Use wrappers for existing tools (python wrapper for subfinder, amass) process and store the results.
2. Seperate wrapper for all other subdomain enumeration tools (subfinder, assetfinder, call an api that produces similar results)
3. wrapper http-prob which target are webservers, nmap or masscan to determine open ports.