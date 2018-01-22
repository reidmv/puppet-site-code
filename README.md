Table of Contents
=================

  * [What You Get From This puppet-code repo](#what-you-get-from-this-puppet-code-repo)

# Where's my Puppetfile?

This repo is does not contain a Puppetfile. Rather, it is intended to be
deployed _by_ a Puppetfile. Nor does this repository have a branch per Puppet
environment. This repo has a normal git "master" branch, and any other branches
or tags needed to implement a typical development workflow.

The Puppetfile is housed in a separate, dedicated repository called
`puppet-deployment`. Each branch of puppet-deployment contains one file only:
the Puppetfile. The Puppetfile in puppet-deployment dictates 100% of the code
to be deployed to a given Puppet environment, and at what version. That
includes _this_ content; the `puppet-site` code, which is deployed directly to
the root of a Puppet environment at the version specified by
puppet-deployment.

# What You Get From This puppet-code repo

This repository is a template puppet-code repo that can be used with the _puppet-deployment workflow_.

The major pieces of content are:
 - An environment.conf that correctly implements:
   - A `site-modules` directory for roles, profiles, and any custom modules for your organization.
   - A config\_version script.
 - Basic example of roles/profiles code.
 - Provided config\_version scripts to output the commit of code that your agent just applied.
 - Sample hiera configuration:
   - `hiera.yaml` to configure a simple hierarchy.
   - `data` directory with pre-created common.yaml and nodes directory.
