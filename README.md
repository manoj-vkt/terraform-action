# terraform-action
Git action for doing terraform plan and apply
# Usage
### Do Plan
```yaml
    - name: Terraform plan
      uses: manoj-vkt/terraform-action@V1.0
      with:
        terraform_version: "1.6.6"
        account_setup_directory: "cloud_infrastructure/cloud_setup"
        environment: "deploy"
        tf_vars_file: "tfvars/dev.tfvars"
        action_to_perform: "plan"
```
### Do Apply
```yaml
    - name: Terraform apply
      uses: manoj-vkt/terraform-action@V1.0
      with:
        terraform_version: "1.6.6"
        account_setup_directory: "cloud_infrastructure/cloud_setup"
        environment: "deploy"
        tf_vars_file: "tfvars/dev.tfvars"
```

| Input name              | Description                                      | Type     | Required | Default              |
|-------------------------|--------------------------------------------------|----------|----------|----------------------|
| terraform_version       | Terraform version to be used in deployment       | `string` | Yes      | N/A                  |
| account_setup_directory | Directory path where terraform files are present | `string` | Yes      | N/A                  |
| environment             | Deployment environment                           | `string` | Yes      | N/A                  |
| tf_vars_file            | File containing terraform variable values        | `string` | Yes      | N/A                  |
| config_file             | Name of the backend config file                  | `string` | No       | `backend-config.hcl` |
| action_to_perform       | Perform plan or apply                            | `string` | No       | `apply`              |
| terraform_parallelism   | Terraform parallelism value                      | `number` | No       | `10`                 |