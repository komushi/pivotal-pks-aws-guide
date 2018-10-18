## 1. Create a Hosted Zone with your domain
* [Hosted Zone](https://console.aws.amazon.com/route53/home#hosted-zones:)
* Domain name used: xulei.app
* The following NS and SOA records will be added automatically

| Name | Type | Value |
| ------------- |:-------------:| -----:|
| xulei.app. | NS | ns-608.awsdns-12.net. <br> ns-1441.awsdns-52.org. <br> ns-1691.awsdns-19.co.uk. <br> ns-197.awsdns-24.com. |
| xulei.app. | SOA | ns-608.awsdns-12.net. awsdns-hostmaster.amazon.com. 1 7200 900 1209600 86400 |


## 2. Add Nameservers at Godaddy Nameservers
Domain Manager -> Manage DNS -> Nameservers(Using custom nameservers)

```
ns-608.awsdns-12.net
ns-1441.awsdns-52.org
ns-1691.awsdns-19.co.uk
ns-197.awsdns-24.com
```

## 3. Request a certificate with your subdomain
* [Certificate Manager](https://console.aws.amazon.com/acm/home)
* Domain name: pks.xulei.app
* Additional names:
```
*.sys.pks.xulei.app, 
*.login.sys.pks.xulei.app, 
*.uaa.sys.pks.xulei.app, 
*.apps.pks.xulei.app 
```
* Validation method: DNS validation
**Using the DNS validation method needs to add CNAME records in Route53 for validation**

