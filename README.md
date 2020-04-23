# quickstart-aws-acm-certificate
This quickstart module takes care of all the moving parts of creating an ACM certificate to declutter other quickstarts with the extra logic required.

## Inputs parameters:
```yaml
    DomainName: my.super.cool.dnsname # FQDN For the certificate
    HostedZoneID: XZXZXXXZZZZZZZ  # AWS R53 HostedZone for DNS verification of domain ownership
```


