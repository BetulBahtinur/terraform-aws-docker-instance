- Go to the `README.md` and make a description of your module.

---
Terraform Module to provision an AWS EC2 instance with the latest amazon linux 2 ami and installed docker in it.

Not intended for production use. It is an example module.

It is just for showing how to create a publish module in Terraform Registry.

Usage:

```hcl

provider "aws" {
  region = "us-east-1"
}

module "docker_instance" {
    source = "<github-username>/docker-instance/aws"
    key_name = "clarusway"
}
```
---

### Create a Github repository for our terraform module

- Create a `public` github repo and name it as `terraform-aws-docker-instance`.

- Clone the repository to your local.

```bash
git clone https://github.com/<your-github-account>/terraform-aws-docker-instance.git
```

- ``Copy`` the module files to this repository folder.

- Next, ``push`` the files to github repo and give a tag to version our module. You should give a semantic version to your module.(https://semver.org/)

```bash
git add .
git commit -m "should define your key file"
git push
git tag v0.0.1
git push --tags
```

- Go to the `Terraform Registry` and sign in with your `Github Account`.

- Next, `Publish` your module.

* Terraform Registry --> Sign in --> Github account --> Publish --> Modules --> Select the module repo in Github (terraform-aws-docker-instance) --> Click Agree in Terms --> Publish Module

- Go to the ``Github Repository``. Define a description in `About` part in github repository. (Click settings wheel)
