## 1. Prerequisites
* [Terrafirn CLI](https://www.terraform.io/intro/getting-started/install.html)
* IAM User with the following permissions
    * AmazonEC2FullAccess
    * AmazonRDSFullAccess
    * AmazonRoute53FullAccess
    * AmazonS3FullAccess
    * AmazonVPCFullAccess
    * IAMFullAccess

## 2. Terraform Variables File
### 2-1. Download AWS Terraform Templates 
* Link: Pivotal Network's [Pivotal Application Service](https://network.pivotal.io/products/elastic-runtime/)
* File Version: AWS Terraform Templates 0.20.0
* File Name: terraforming-aws-0.20.0.zip

### 2-2.
* Extract the terraforming-aws-0.20.0.zip as a folder
* Create terraform.tfvars under the folder

```
env_name           = "pks"
access_key         = "YOUR-ACCESS-KEY"
secret_key         = "YOUR-SECRET-KEY"
region             = "ap-northeast-1"
availability_zones = ["ap-northeast-1a", "ap-northeast-1c", "ap-northeast-1d"]
ops_manager_ami    = "ami-0c94c92ee43d55e92"
dns_suffix         = "xulei"

ssl_cert = <<SSL_CERT
-----BEGIN CERTIFICATE-----
YOUR-CERTIFICATE
-----END CERTIFICATE-----
SSL_CERT

ssl_private_key = <<SSL_KEY
-----BEGIN EXAMPLE RSA PRIVATE KEY-----
YOUR-PRIVATE-KEY
-----END EXAMPLE RSA PRIVATE KEY-----
SSL_KEY

```