# Delphix Host Postgres Packer Template

This Packer template will create an Amazon Web Service AMI configured as a Delphix ready Postgresql server. It uses Amazon Linux 2.0 and Postgres 9.6.

#### Table of Contents
1.  [Installation](#installation)
2.  [Usage](#usage)
3.  [Links](#links)
4.  [Contribute](#contribute)
    *   [Code of conduct](#code-of-conduct)
    *   [Community Guidelines](#community-guidelines)
    *   [Contributor Agreement](#contributor-agreement)
5.  [Reporting Issues](#reporting-issues)
6.  [Statement of Support](#statement-of-support)
7.  [License](#license)

## <a id="installation"></a>Installation

After Packer and the AWS CLI tools are installed (see [Links](#links) section), create environment variables for `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, and `AWS_REGION`. Alternatively, you can run `aws configure` to set up the AWS CLI. Packer will use this in lieu of ENV variables.


```bash
export AWS_ACCESS_KEY_ID = ***your aws access key id***
export AWS_SECRET_ACCESS_KEY = ***your aws access secret key***
export AWS_REGION = ***your aws region***

```

Clone the repo into a working directory

```bash
git clone https://github.com/delphix/packer-postgres-host-template
cd packer-postgres-host-template
```

## <a id="usage"></a>Usage

After Packer and AWS CLI are installed, navigate to the working directory and run:

```bash
packer build main.json
```

This will build an AMI names `delphix-postgres-` followed by a timestamp. After the AMI is created, you will be able to launch and EC2 instance from it. Once the EC2 instance is running, `postgres` will be installed and running. You should login as the postgres user and set a password.

## <a id="links"></a>Links

*   [Getting Started with Packer](https://www.packer.io/intro/index.html)
*   [AWS Command Line](https://aws.amazon.com/cli/)

## <a id="contribute"></a>Contribute

1.  Fork the project.
2.  Make your bug fix or new feature.
3.  Add tests for your code.
4.  Send a pull request.

Contributions must be signed as `User Name <user@email.com>`. Make sure to [set up Git with user name and email address](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup). Bug fixes should branch from the current stable branch. New features should be based on the `master` branch.

#### <a id="code-of-conduct"></a>Code of Conduct

This project operates under the [Delphix Code of Conduct](https://delphix.github.io/code-of-conduct.html). By participating in this project you agree to abide by its terms.

#### <a id="contributor-agreement"></a>Contributor Agreement

All contributors are required to sign the Delphix Contributor agreement prior to contributing code to an open source repository. This process is handled automatically by [cla-assistant](https://cla-assistant.io/). Simply open a pull request and a bot will automatically check to see if you have signed the latest agreement. If not, you will be prompted to do so as part of the pull request process.


## <a id="reporting_issues"></a>Reporting Issues

Issues should be reported [here](https://github.com/delphix/packer-postgres-host-template/issues).

## <a id="statement-of-support"></a>Statement of Support

This software is provided as-is, without warranty of any kind or commercial support through Delphix. See the associated license for additional details. Questions, issues, feature requests, and contributions should be directed to the community as outlined in the [Delphix Community Guidelines](https://delphix.github.io/community-guidelines.html).

## <a id="license"></a>License

This is code is licensed under the Apache License 2.0. Full license is available [here](./LICENSE).
