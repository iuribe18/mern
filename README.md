# Automate Deploys AWS Infrastructure with Terraform using GitHub actions

### Step 1: Clone the repository in the local machine
```
git clone https://github.com/bjnandi/terraform-ci-cd-aws.git
```

### Step 2: Set up HCP Terraform Cloud

```
Organization > Workspaces > Variables
```

### Step 3: Create an API token

Generate an HCP Terraform user API token. For this go to the Tokens page in HCP Terraform User Settings. Click on Create an API token, enter the GitHub Actions token for the Description, then click “Generate token”.

### Step 4: Set up an API token to the GitHub repository in GitHub Secrets.
You can read GitHub Secrets for more details. Now we go to secrets and variables and set values.
```
Github > Repo Name > Settings > Secrets and variables > Action > Repository Secrets > New repository secret 
```

### Step 5: Return to the VS Code Editor & create a new branch in our repository named “tf-infa-test”.

```
git checkout -b 'tf-infa-test'
```

### Step 6: I added “env/dev” in the Terraform Working Directory in HCP Terraform Cloud.

```
env/dev
```

### Step 7: Create a pull request
Now, Return to the VS Code Editor & Minor changes in the code for the demo test then commit & push the code in the GitHub “tf-infa-test” branch. Create a pull request for this branch in GitHub.

After the pull request run a GitHub workflow (Terraform plan) to check the Terraform plan.

### Step 8: Review and merge the pull request

If you are satisfied with the “Terraform plan” then close the “pull request” with the “merge” code in the ‘main’ branch then run a workflow (Terraform apply) for provisioning infrastructure.

### Step 9: Verify the EC2 instance provisioned
All resources have been created.

### Learn More Here
[Build an End-to-End CI/CD Pipeline for a MERN App in Kubernetes with Terraform using GitHub Actions & Ansible](https://medium.com/aws-in-plain-english/build-an-end-to-end-ci-cd-pipeline-for-mern-app-terraform-using-github-actions-with-ansible-d7686ccc8db1)

Happy coding! 💻✨

