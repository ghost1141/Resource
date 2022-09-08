Bug bounty Resources
Recon

    Assetfinder - Find domains and subdomains potentially related to a given domain.
    Subfinder - subdomain discovery tool
    Prips - tool that can be used to print all of the IP address on a given range
    JQ - https://stedolan.github.io/jq/
    Hakrevdns - simple tool for performing reverse DNS lookups
    Massdns - simple high-performance DNS stub resolver
    Shuffledns - https://github.com/projectdiscovery/shuffledns
    Project Discovery Chaos - https://chaos.projectdiscovery.io/#/
    AMASS - https://github.com/OWASP/Amass
    LazyRecon - https://github.com/nahamsec/lazyrecon

Magic Checklist

Bug bounty ToDo list by soyelmago
Workflows compilation
Subdomain live checker

# toma como parametro el archivo con las urls
# ejemplo: python3 list_websites.py subfinder_starlink.txt
import sys
import subprocess

with open(sys.argv[1]) as fp:
    for line in fp:
        print("voy a probar:" + line.strip())
        subprocess.call(["curl", "-i", "--connect-timeout", "5", line.strip()])
        sys.stdout.flush()
