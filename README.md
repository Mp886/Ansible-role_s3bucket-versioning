Role Name
=========

This Ansible role enforces versioning on specific S3 buckets in an AWS account.

Requirements
------------

- Ansible 2.9 or higher
- boto3
- AWS credentials with appropriate permissions to list and modify S3 buckets

You can install the required Python packages using:

command: pip install boto3

Ensure that your AWS credentials are configured properly. You can configure them using the AWS CLI:

command: aws configure

Role Variables
--------------

The following variables are available for this role:

target_buckets: A list of S3 bucket names on which versioning should be enabled. This variable must be defined either inthe playbook or in the role's vars file.

target_buckets:
  - bucket-name
  - another-bucket-name

Dependencies
------------

This role does not have any dependencies on other roles.

Example Playbook
----------------

- name: Enforce S3 bucket versioning on specific AWS buckets
  hosts: localhost
  gather_facts: false

  roles:
    - policy-as-code

