# Dynatrace configuration via API using ansible

This repository contains API definitions and playbooks for the dynatrace API that can be used for automating the creation and updating of monitoring configurations and adapting the monitoring as code methodology.

## Prerequisites

- Ansible installed
- The environment URL: Managed `https://{your-domain}/e/{your-environment-id}` | SaaS `https://{your-environment-id}.live.dynatrace.com`
- The API token of your environment for authenticating with the dynatrace API
