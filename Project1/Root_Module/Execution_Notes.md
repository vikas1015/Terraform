### In this section we are going to create below files

* main.tf
* variables.tf
* outputs.tf
* terraform.tfvars

## Environment Setup
cd ~/terraform/AWS \
touch {main.tf,variables.tf,outputs.tf,terraform.tfvars}

## Write code for main.tf, variables.tf, outputs.tf, terraform.tfvars

## Initiatlize terraform
export AWS_ACCESS_KEY_ID="[ACCESS_KEY]" \
export AWS_SECRET_ACCESS_KEY="[SECRET_KEY]]" \
terraform init

## Validate Code
terraform validate

**We don't require to do terraform plan step as we are using terraform.tfvars file**

## Deploy the S3 bucket
terraform apply -auto-approve

## Destroy S3 bucket
terraform destroy -auto-approve
