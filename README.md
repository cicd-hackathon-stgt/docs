Criteria for selecting CI/CD tools
==================================

Here's a collection of thoughts regarding how to chose a CI/CD tool that fits your needs.


Documentation
-------------

* is the overall concept documented and easy-to-understand
* does usage of tool provide enough blog posts / SO posts / tutorials / videos


Setup & Maintenance
-------------------

* Packages (`.rpm`, `.deb`...) available (and maintained)
* Docker images available (and maintained)
* Proper update workflow (zero downtime)
* Installer for (public) cloud environments (BOSH manifest, Terrarform, Ansible, Chef, ...)


Configuration
-------------

* GUI-only config or files (that can be put in version control...)


User Management
---------------

* LDAP connection
* Granularity of roles / permissions


Credentials Management
----------------------

* Internal credentials store
* Connection to external store (credhub, vault, ...)
* are credentials securely injected into your jobs


Job Runners
-----------

* Scalability of runners (auto-scale)
* Integration of Docker
* running on arbitrary machines (even local laptop)
* do runners cover all OSes that you need (i.e. Windows, Mac)
* can runners easily be set up (with your build tools)
* are environments separated (each tech stack has its own runner)


Pipelines
---------

* Support of Pipelines
* Pipelines as code
* DSL (Groovy...) or YAML
* fan-in / fan-out
* can tasks be shared in libraries
* can pipelines be generated via CLI tool / automated


Integration in SCM
------------------

* feedback on every commit (builds / doesn't build), visible in SCM
* check merge / pull requests
* automatically create jobs for branches
* scan ORGs / groups for projects, automatically create jobs (e.g. Jenkins Github integration)
