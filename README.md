## Purpose

This Packer AMI Builder creates a new AMI out of the latest Amazon Linux AMI.

TODO - write a build diagram with yEd and insert it here.

## Source code structure

```bash
├── ansible
│   ├── playbook.yaml                       <-- Ansible playbook file
│   ├── requirements.yaml                   <-- Ansible Galaxy requirements containing additional Roles to be used (CIS, Cloudwatch Logs)
│   └── roles
│       ├── common                          <-- Upgrades all packages through ``yum``
├── buildspec.yml                           <-- CodeBuild spec 
├── packer_cis.json                         <-- Packer template
```

## CDK Deployment to AWS Batch
TODO - Deployment of the AMI to AWS Batch for automated testing and developer use with ssh/vscode.

## HOWTO

**Before you start**

* Either have your application code in an S3 bucket or an AWS supported git host.
* Make sure your CodeBuild instance S3 read/write access.
* Make sure your CodeBuild instance has permissons set for enhanced privlidges so it can run Docker containers.

