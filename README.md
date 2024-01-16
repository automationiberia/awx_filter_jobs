
# Get List Jobs

## Brief Description

This playbook provides a foundation for retrieving and displaying information about AWX jobs, with the flexibility to extract and display specific details based on your needs. Adjust the playbook and variables according to your specific requirements.

### Installing awx.awx Ansible Collection

To use the provided playbook, you need to install the `awx.awx` Ansible collection. Run the following command:

```bash
ansible-galaxy collection install awx.awx
```

### Get Jobs List
```bash
ansible-playbook awx_filter_jobs.yaml -e '{launched_by_user: awx-org-user, job_status: successful}'
```

| Variable               | Description                                                                                   |
|------------------------|-----------------------------------------------------------------------------------------------|
| `controller_host`      | The hostname or IP address of the AWX or Ansible Tower instance.                               |
| `controller_username`  | The username used to authenticate to the AWX or Ansible Tower instance.                         |
| `controller_password`  | The password used to authenticate to the AWX or Ansible Tower instance.                         |
| `validate_certs`       | A boolean indicating whether to validate SSL certificates. Set to `false` to disable certificate validation. |
| `status`               | The status of jobs to filter. It could be set to a specific status like `"successful"` or `"failed"`. |
| `all_pages`            | A boolean indicating whether to retrieve all pages of job results. Set to `true` to ensure all job information is collected. |
| `launched_by_user`     | A variable to specify the username for filtering jobs based on the user who launched them.     |

