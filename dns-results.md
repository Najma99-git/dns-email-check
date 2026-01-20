## Task 1
Command to use:
dig bbc.co.uk MX
```test
bbc.co.uk.              300     IN      MX      10 cluster1.eu.messagelabs.com.
bbc.co.uk.              300     IN      MX      20 cluster1a.eu.messagelabs.com

## Task 2
Command to use
dig bbc.co.uk TXT
dig @8.8.8.8 bbc.co.uk TXT 
```test
"v=spf1 ip4:212.58.224.0/19 ip4:132.185.0.0/16 +include:spf.sis.bbc.
NOTE:
dig bbc.co.uk failed at first. I thought DNS resolution is failing due to an unreachable configured nameserver. Then I tried to bybass by forcing dig to use google DNS directly.
TXT records for bbc.co.uk were successfully retrieved using a public DNS resolver; email-related TXT records (SPF) are present.
