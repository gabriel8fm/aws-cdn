# CDN to static site hosting

This project creates a complete static site hosting. To this purpose we use these AWS services:

- Cloudfront
- S3
- ACM
- Route 53

#### Directory Structure

! [Directory Structure] (img/tree.png)

#### Modules

* ** Cloudfront **

Responsible to creating the CDN configuration.

* ** S3 **

Creates a public S3 bucket.

* ** ACM **

Reponsible to enable custom certificates to the static website.

* ** main.tf **

Root configuration about providers and modules that will be necessary.

#### Terraform Init

Note: Before starting the terraform commands, it is important to have configured the `hosted zone` in route53 with the domain that will be used in this module, after making this configuration just inform the domain in the` main.tf` file.

First you will have to configure your AWS credentials on this file `/ home / user / .aws / credentials`. Then run:

> terraform init

This command will install all modules dependencies.

#### Terraform Plan

To validate the resources that will be create on AWS account, run this:

> terraform plan

#### Terraform Apply

If your validation was ok, then you can create all resources running this:

> terraform apply

Once successfully completed, simply upload an `index.html` file into the bucket and attempt access via CDN endpoint.

#### Terraform Destroy

OMG, I don't like this... then run::

> terraform destroy

#### References

[Terraform] (https://learn.hashicorp.com/terraform)
[cloudfront] (https://aws.amazon.com/cloudfront/)
[S3] (https://aws.amazon.com/en/s3/)
[ACM] (https://aws.amazon.com/certificate-manager/)
[route53] (https://aws.amazon.com/route53/)
