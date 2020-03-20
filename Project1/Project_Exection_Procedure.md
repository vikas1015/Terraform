# Tf Storage module: The S3 Bucket and Random ID

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
