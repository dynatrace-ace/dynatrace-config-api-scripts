# Creating or updating a web application and an application detection rule

## Prerequisites

Create an inventory file with the required dynatrace environment URL and API token.

```bash
localhost:
  hosts:
    localhost:
  vars:
    ansible_connection: local
    dt_environment_url: https://{your-environment-id}.live.dynatrace.com
    dt_environment_id: {your-environment-id}
    dt_api_token: {your-api-token}
```

## Run the playbook

The following command can be executed to create the application along with its detection rule:

```bash
ansible-playbook create_update_app.yml -i inventory.yml --extra-vars "app_name='test app' url_pattern=http://192.168.22.23"
```

Depending on the inventory file, state files will be created on the state/ dir with the app id that will be used for updating already existing configurations as well as creating or updating app detection rules.

The create_update_app.yml playbook will include the tasks from the create_update_app_det_rule.yml in the application-detection-rules-api/ dir and a state file will also be stored in application-detection-rules-api/state/ for that specific configuration.
