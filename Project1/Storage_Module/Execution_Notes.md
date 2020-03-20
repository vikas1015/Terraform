# In this Project - 1 we will creating 4 Terraform Modules. The below 3 modules are glued to "Root Module".
* Root Module
* Storage Module
* Network Module
* Compute Module

# Tf Storage module: The S3 Bucket and Random ID

## Environment setup
mkdir -p ~/terraform/AWS/storage \
cd ~/terraform/AWS/storage

** Create main.tf, variables.tf, output.tf and then follow below steps **

## Initialize Terraform
terraform init

## Validate Changes
terraform validate

## Plan the changes
export AWS_ACCESS_KEY_ID="[ACCESS_KEY]" \
export AWS_SECRET_ACCESS_KEY="[SECRET_KEY]" \
export AWS_DEFAULT_REGION="us-east-1" \
terraform plan -out=tfplan -var project_name=la-terraform

## Deploy the S3 bucket
terraform apply tfplan

## Destroy the S3 bucket
terraform destroy -auto-approve -var project_name=la-terraform
