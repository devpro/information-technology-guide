# GitLab pipelines

🌐 [CI/CD pipelines](https://docs.gitlab.com/ee/ci/pipelines/)

## Core feature

* [CI/CD YAML syntax reference](https://docs.gitlab.com/ee/ci/yaml/)
* [Services](https://docs.gitlab.com/ee/ci/services/)
* [Downstream pipelines](https://docs.gitlab.com/ee/ci/pipelines/downstream_pipelines.html)
* [GitLab Runner Autoscaling](https://docs.gitlab.com/runner/runner_autoscale/)
* [CI/CD Catalog](https://gitlab.com/explore/catalog)
* [GitLab components](https://gitlab.com/components)

## Best practices

* Job fields: `before_script`, `script`, `after_script`
* [Optimize configuration files](https://docs.gitlab.com/ee/ci/yaml/yaml_optimization.html) (Anchors, `extends`, `!reference`)
* [Use configuration from other files](https://docs.gitlab.com/ee/ci/yaml/includes.html) (`include`)
* [Caching](https://docs.gitlab.com/ee/ci/caching/)

See also [10 préconisations pour une CI/CD efficace](https://www.linkedin.com/pulse/gitlab-ci-10-pr%C3%A9conisations-pour-une-cicd-efficace-benoit-couetil/)

## Security concerns

* [How to scan a full commit history to detect sensitive secrets](https://about.gitlab.com/blog/2025/02/06/how-to-scan-a-full-commit-history-to-detect-sensitive-secrets/)
* [Tutorial: Security scanning in air-gapped environments](https://about.gitlab.com/blog/2025/02/05/tutorial-security-scanning-in-air-gapped-environments/)

## Debugging

* [Run a pipeline in a container](runner-container.md#debug-pipeline-with-local-execution)
* [Troubleshooting GitLab Runner](https://docs.gitlab.com/runner/faq/index.html)
