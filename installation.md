```
1. Terraform Installation
This section details how to install Terraform using the official HashiCorp RPM repository.

Install repository utilities: Install yum-utils (which provides yum-config-manager) and unzip.

sudo yum install -y yum-utils unzip
# OR (if using dnf)
# sudo dnf install -y dnf-utils unzip
Add the official HashiCorp repository:

sudo yum-config-manager --add-repo https://rpm.releases.hashicorp.com/RHEL/hashicorp.repo
Install Terraform:

sudo yum install -y terraform
# OR (if using dnf)
# sudo dnf install -y terraform
Verify the installation:

terraform --version
2. AWS Command Line Interface (AWS CLI v2)
Use the official AWS installer bundle for a clean installation.

Download and extract the installer:

curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
Run the installation script: This installs the AWS CLI to /usr/local/aws-cli by default.

sudo ./aws/install
Clean up installer files:

rm -rf awscliv2.zip aws
Configure AWS credentials and region:

aws configure
Verify access:

aws sts get-caller-identity
3. Infracost Installation (Optional)
Install Infracost for cloud cost estimates.

Run the official installation script:
curl -fsSL https://raw.githubusercontent.com/infracost/infracost/master/scripts/install.sh | sh

```
