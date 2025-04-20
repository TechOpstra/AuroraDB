# AuroraDB
<!-- BEGIN_TF_DOCS -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.1.0 |
| <a name="requirement_aws"></a> [aws](#requirement\_aws) | ~> 5.94.1 |

## Providers

No providers.

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_aurora_db_setup"></a> [aurora\_db\_setup](#module\_aurora\_db\_setup) | ./modules/aurora | n/a |

## Resources

No resources.

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_allowed_inbound_cidrs"></a> [allowed\_inbound\_cidrs](#input\_allowed\_inbound\_cidrs) | List of CIDR blocks allowed to access the AuroraDB | `list(string)` | <pre>[<br/>  "10.0.0.0/8"<br/>]</pre> | no |
| <a name="input_aurora_cluster_name"></a> [aurora\_cluster\_name](#input\_aurora\_cluster\_name) | The name of the Aurora cluster | `string` | `"aurora-db-cluster"` | no |
| <a name="input_availability_zones"></a> [availability\_zones](#input\_availability\_zones) | List of Availability Zones for subnets | `list(string)` | <pre>[<br/>  "us-east-1a",<br/>  "us-east-1b",<br/>  "us-east-1c"<br/>]</pre> | no |
| <a name="input_database_name"></a> [database\_name](#input\_database\_name) | The initial database name | `string` | `"mydb"` | no |
| <a name="input_db_engine"></a> [db\_engine](#input\_db\_engine) | The database engine type | `string` | `"aurora-mysql"` | no |
| <a name="input_db_engine_version"></a> [db\_engine\_version](#input\_db\_engine\_version) | The database engine version | `string` | `"8.0.mysql_aurora.3.05.2"` | no |
| <a name="input_db_instance_type"></a> [db\_instance\_type](#input\_db\_instance\_type) | The instance type for Aurora nodes | `string` | `"db.t4g.medium"` | no |
| <a name="input_db_master_password_length"></a> [db\_master\_password\_length](#input\_db\_master\_password\_length) | Length of the generated master password | `number` | `16` | no |
| <a name="input_db_master_username"></a> [db\_master\_username](#input\_db\_master\_username) | The master username for the Aurora cluster | `string` | `"admin"` | no |
| <a name="input_db_port"></a> [db\_port](#input\_db\_port) | The port the database listens on | `number` | `3306` | no |
| <a name="input_project_name"></a> [project\_name](#input\_project\_name) | A unique name for the project | `string` | `"auroradb1"` | no |
| <a name="input_region"></a> [region](#input\_region) | AWS region to deploy to | `string` | `"us-east-1"` | no |
| <a name="input_secrets_manager_secret_name"></a> [secrets\_manager\_secret\_name](#input\_secrets\_manager\_secret\_name) | The name of the secret in AWS Secrets Manager | `string` | `"aurora-db-credentials"` | no |
| <a name="input_vpc_cidr"></a> [vpc\_cidr](#input\_vpc\_cidr) | CIDR block for the VPC | `string` | `"10.0.0.0/16"` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_aurora_endpoint"></a> [aurora\_endpoint](#output\_aurora\_endpoint) | n/a |
| <a name="output_secrets_manager_secret_arn"></a> [secrets\_manager\_secret\_arn](#output\_secrets\_manager\_secret\_arn) | n/a |
| <a name="output_security_group_id"></a> [security\_group\_id](#output\_security\_group\_id) | n/a |
| <a name="output_vpc_id"></a> [vpc\_id](#output\_vpc\_id) | n/a |
<!-- END_TF_DOCS -->