### 1\. Terraform Installation

This section details how to install Terraform using the official HashiCorp RPM repository.

1.  **Install repository utilities:**
    Install `yum-utils` (which provides `yum-config-manager`) and `unzip`.

    ```bash
    sudo yum install -y yum-utils unzip
    # OR (if using dnf)
    # sudo dnf install -y dnf-utils unzip
    ```

2.  **Add the official HashiCorp repository:**

    ```bash
    sudo yum-config-manager --add-repo https://rpm.releases.hashicorp.com/RHEL/hashicorp.repo
    ```

3.  **Install Terraform:**

    ```bash
    sudo yum install -y terraform
    # OR (if using dnf)
    # sudo dnf install -y terraform
    ```

4.  **Verify the installation:**

    ```bash
    terraform --version
    ```

-----

### 2\. AWS Command Line Interface (AWS CLI v2)

Use the official AWS installer bundle for a clean installation.

1.  **Download and extract the installer:**

    ```bash
    curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
    unzip awscliv2.zip
    ```

2.  **Run the installation script:**
    This installs the AWS CLI to `/usr/local/aws-cli` by default.

    ```bash
    sudo ./aws/install
    ```

3.  **Clean up installer files:**

    ```bash
    rm -rf awscliv2.zip aws
    ```

4.  **Configure AWS credentials and region:**

    ```bash
    aws configure
    ```

5.  **Verify access:**

    ```bash
    aws sts get-caller-identity
    ```

-----

### 3\. Infracost Installation (Optional)

Install Infracost for cloud cost estimates.

  * **Run the official installation script:**
    ```bash
    curl -fsSL https://raw.githubusercontent.com/infracost/infracost/master/scripts/install.sh | sh
    ```
