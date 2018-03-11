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


On-premise vs. SaaS
-------------------

* do you need an on-prem solution
* could it be SaaS solution
* do you "only" build stuff, or also deploy stuff


OSS vs. Commercial products
---------------------------

* how big is the community around the tool
* popularity of tool (last commits, stars on Github, issues opened vs. closed...)
* do you need (commercial) support


Configuration
-------------

* GUI-only config or files (that can be put in version control...)


User Management
---------------

* LDAP integration
* multi-tenancy capabilities
* Granularity of roles / permissions
* can user / roles management be stored in files or only via GUI
* SSO with Github, Gitlab, ...


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
* uni-directional vs. bi-directional communication between master and agents
* do runners cover all OSes that you need (i.e. Windows, Mac)
* can runners easily be set up (with your build tools)
* are environments separated (each tech stack has its own runner)
* do jobs survive a restart of the master


Pipelines
---------

* Support of Pipelines
* Pipelines as code
* DSL (Groovy...) or YAML
* fan-in / fan-out
* can tasks be shared in libraries
* can pipelines be generated via CLI tool / automated
* are manual approval / input steps provided


Job Configuration
-----------------

* grouping jobs in folders / groups
* templates for job configuration re-use


API / CLI tools
---------------

* can tool be accessed / configured / extended via API / CLI
* what features are exposed as API
* what about multi-tenancy / permission management of API


Integration in SCM
------------------

* feedback on every commit (builds / doesn't build), visible in SCM
* check merge / pull requests
* automatically create jobs for branches
* scan ORGs / groups for projects, automatically create jobs (e.g. Jenkins Github integration)
* grant permissions to build jobs based on SCM permissions


Traceability / Ticketing system
-------------------------------

* Linking / tracing of artifacts from ticket to scm commit to release to deployment
* Integration in ticketing system like JIRA - show build state, group builds, close / open tickets


Dashboards, Notifications, Monitoring, Logs
-------------------------------------------

* are useful, configurable dashboards provided
* is monitoring of disk usage, CPU, ... provided (e.g. integration in Prometheus...)
* what about rotating logs, deleting old artifacts, clean up of broken builds
* integration in chat servers like Slack, HipChat, Mattermost or RocketChat
* email notifications - possibility to manage groups of people that are notified
* reports on code quality, test results, performance tests
* given a broken build: how fast can you figure out, why it broke


Extensibility
-------------

* plugins / vs. plugin hell
* how to check new plugins before upgrade
* how well are extension points documented
* can product be extended without plugins (e.g. Concourse resources)


Rerferences
===========

* http://dannyvarner.com/2017/08/11/how-to-choose-a-continuous-integration-tool.html
* https://stackify.com/top-continuous-integration-tools/
* https://blog.sqreen.io/how-to-choose-your-ci-tool/
