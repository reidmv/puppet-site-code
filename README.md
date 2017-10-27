Table of Contents
=================

  * [What You Get From This puppet-site-code repo](#what-you-get-from-this-puppet-site-code-repo)

# What You Get From This puppet-site-code repo

This repository is a template puppet-site-code repo that can be used with the _puppet-deployment workflow_.

The major pieces of content are:
 - An environment.conf that correctly implements:
   - A `site-modules` directory for roles, profiles, and any custom modules for your organization.
   - A config\_version script.
 - Provided config\_version scripts to output the commit of code that your agent just applied.
 - Basic example of roles/profiles code.
 - Sample hiera configuration:
   - `hiera.yaml` to configure a simple hierarchy.
   - `data` directory with pre-created common.yaml and nodes directory.
