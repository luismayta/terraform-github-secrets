<!--


  ** DO NOT EDIT THIS FILE
  **
  ** 1) Make all changes to `README.yaml`
  ** 2) Run`make readme` to rebuild this file.
  **
  ** (We maintain HUNDREDS of open source projects. This is how we maintain our sanity.)
  **


  -->

# terraform-github-secrets

[![Lint](https://github.com/hadenlabs/terraform-github-secrets/actions/workflows/lint.yml/badge.svg?branch=develop)](https://github.com/hadenlabs/terraform-github-secrets/actions) [![Issues](https://img.shields.io/github/issues/hadenlabs/terraform-github-secrets.svg)](https://github.com/hadenlabs/terraform-github-secrets/issues) [![Latest Release](https://img.shields.io/github/release/hadenlabs/terraform-github-secrets.svg)](https://github.com/hadenlabs/terraform-github-secrets/releases)

secrets terraform

## Usage

```hcl
  module "main" {
    source = "hadenlabs/secrets/github"
    version = "0.1.1

    providers = {
      github = github
    }

    visibility        = "all"
    secrets = {
      GH_TOKEN = "token"
    }

  }

```

Full working examples can be found in [examples](./examples) folder.

## Examples

### common

```hcl
    module "main" {
      source = "hadenlabs/secrets/github"
      version = "0.1.1

      providers = {
        github = github
      }

      visibility        = "all"
      secrets = {
        GH_TOKEN = "token"
      }

    }

```

 <!-- BEGIN_TF_DOCS -->

## Requirements

| Name                                                                     | Version |
| ------------------------------------------------------------------------ | ------- |
| <a name="requirement_terraform"></a> [terraform](#requirement_terraform) | >= 0.14 |
| <a name="requirement_github"></a> [github](#requirement_github)          | >=4.5.0 |

## Providers

| Name                                                      | Version |
| --------------------------------------------------------- | ------- |
| <a name="provider_github"></a> [github](#provider_github) | >=4.5.0 |

## Modules

No modules.

## Resources

| Name | Type |
| --- | --- |
| [github_actions_organization_secret.this](https://registry.terraform.io/providers/integrations/github/latest/docs/resources/actions_organization_secret) | resource |

## Inputs

| Name | Description | Type | Default | Required |
| --- | --- | --- | --- | :-: |
| <a name="input_secrets"></a> [secrets](#input_secrets) | secrets for repository | `map(any)` | n/a | yes |
| <a name="input_visibility"></a> [visibility](#input_visibility) | The visibility of the secrets. | `string` | n/a | yes |

## Outputs

| Name                                                     | Description                                         |
| -------------------------------------------------------- | --------------------------------------------------- |
| <a name="output_secret"></a> [secret](#output_secret)    | output instance github actions secrets organization |
| <a name="output_secrets"></a> [secrets](#output_secrets) | List of secrets available.                          |

<!-- END_TF_DOCS -->

## Help

**Got a question?**

File a GitHub [issue](https://github.com/hadenlabs/terraform-github-secrets/issues).

## Contributing

### Bug Reports & Feature Requests

Please use the [issue tracker](https://github.com/hadenlabs/terraform-github-secrets/issues) to report any bugs or file feature requests.

### Development

In general, PRs are welcome. We follow the typical "fork-and-pull" Git workflow.

1.  **Fork** the repo on GitHub
2.  **Clone** the project to your own machine
3.  **Commit** changes to your own branch
4.  **Push** your work back up to your fork
5.  Submit a **Pull Request** so that we can review your changes

**NOTE:** Be sure to rebase the latest changes from "upstream" before making a pull request!

## Module Versioning

This Module follows the principles of [Semantic Versioning (SemVer)](https://semver.org/).

Using the given version number of `MAJOR.MINOR.PATCH`, we apply the following constructs:

1. Use the `MAJOR` version for incompatible changes.
1. Use the `MINOR` version when adding functionality in a backwards compatible manner.
1. Use the `PATCH` version when introducing backwards compatible bug fixes.

### Backwards compatibility in `0.0.z` and `0.y.z` version

- In the context of initial development, backwards compatibility in versions `0.0.z` is **not guaranteed** when `z` is increased. (Initial development)
- In the context of pre-release, backwards compatibility in versions `0.y.z` is **not guaranteed** when `y` is increased. (Pre-release)

## Copyright

Copyright © 2018-2021 [Hadenlabs](https://hadenlabs.com)

## Trademarks

All other trademarks referenced herein are the property of their respective owners.

## License

The code and styles are licensed under the MIT license [See project license.](LICENSE).

## Don't forget to 🌟 Star 🌟 the repo if you like terraform-github-secrets

[Your feedback is appreciated](https://github.com/hadenlabs/terraform-github-secrets/issues)
