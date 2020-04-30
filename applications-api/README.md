# Creating or updating a web application and an application detection rule

## Prerequisites

Create an inventory file with the required dynatrace environment URL and API token.

e.g.

```bash
localhost:
  hosts:
    localhost:
  vars:
    ansible_connection: local
    dt_environment_url: https://{your-environment-id}.live.dynatrace.com
    dt_api_token: {your-api-token}
```

## Run the playbook

The following command can be executed to create the application along with its detection rule:

```bash
ansible-playbook create_update_app.yml -i ../jwl50038.yml --extra-vars "app_name='test app' url_pattern=http://192.168.22.23"
```
