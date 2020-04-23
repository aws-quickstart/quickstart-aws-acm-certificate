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

## Ideas for improvements:
- Support region flag to create Certificates in a specific region (eg: CloudFront requires certificates in us-east-1)
- Do upsert NOT insert in the DNS Hosted Zone so as not to break Domain ownership checks if a Certificate with the same name exists in another region.
- Add logic to the DELETE to not whack the DNS Hosted Zone verfication if another certificate of the same name exists in another region (Poll all regions for this)