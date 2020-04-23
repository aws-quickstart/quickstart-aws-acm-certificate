# quickstart-aws-acm-certificate
This quickstart module takes care of all the moving parts of creating an ACM certificate to declutter other quickstarts with the extra logic required.

## Inputs parameters:
```yaml
    DomainName: my.super.cool.dnsname  # FQDN For the ACM Certificate
    HostedZoneID: XZXZXXXZZZZZZZ  # AWS R53 HostedZone for DNS verification of domain ownership 
    QSS3BucketName: aws-quickstart  # The consuming QuickStart
    QSS3BucketRegion: us-east-1  # The consuming QuickStart 
    QSS3BucketPrefix: quickstart-dfsfdsdfsf  # The consuming QuickStart
```

To use e-mail verification of the Domain please leave Hosted Zone ID blank.