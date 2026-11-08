# Deploying WordPress on AWS Cloud

> Designing highly available architectures on AWS.

A hands-on workshop from the [AWS First Cloud Journey](https://github.com/vanhoangkha/aws-first-cloud-journey) series, available in English and Vietnamese.

**Read the workshop online:** https://vanhoangkha.github.io/000101-HAworkshop/

## Overview

In this lab, you will learn and implement WordPress deployment on AWS Cloud. Practice creating and installing WordPress on EC2 Instance on public subnet connecting to Database Database in private subnet in VPC. This lab ensures that the WordPress application has the ability to scale when encountering a large number of requests and has the ability to balance the load when more than one server is running. Database deployed Multi AZ provides the ability to ensure database availability when deployed.

Amazon CloudFront is a content delivery network (CDN) service built for high-performance, secure user experience.

## Workshop contents

1. Introduction
2. Preparation steps
   - Preparing VPC and Subnet
   - Create Security Group for EC2
   - Create Security Group for Database Instance
   - Initiating EC2 Instance
   - Launch Database Instance
3. Installing wordpress on EC2
4. Implement Autoscaling for wordpress Instance
   - Initialize AMI from Webserver Instance
   - Launch Template
   - createtg
   - Create Load Balancer
   - Create Auto Scaling Group
5. Backup and restore database
   - Create DB snapshot
   - Restore with DB snapshot
6. Create Cloudfront for Web Server
7. Clean up resources

## Prerequisites

- An AWS account with permissions to create the resources used in the labs
- Basic familiarity with the AWS Management Console
- [Hugo](https://gohugo.io/installation/) (extended edition) if you want to run the site locally

## Run locally

```bash
git clone --recurse-submodules https://github.com/vanhoangkha/000101-HAworkshop.git
cd 000101-HAworkshop
hugo server
```

Then open http://localhost:1313 in your browser.

## Repository structure

| Path | Purpose |
| --- | --- |
| `content/` | Workshop pages (`*.md` English, `*.vi.md` Vietnamese) |
| `static/` | Images and other static assets |
| `layouts/` | Hugo layout overrides |
| `themes/` | Hugo theme |
| `config.toml` | Site configuration |

## Cost and cleanup

The labs create AWS resources that may incur charges. Complete the **Clean up** chapter when you finish to remove them.

## Contributing

Contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

To report a security issue, see [SECURITY.md](SECURITY.md).

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE).
