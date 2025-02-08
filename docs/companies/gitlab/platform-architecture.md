# GitLab Platform Architecture

## Components

Name       | Role
-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------
[**Gitaly**](https://gitlab.com/gitlab-org/gitaly) | Gitaly provides high-level RPC access to Git repositories ([docs.gitlab.com/administration/gitaly](https://docs.gitlab.com/ee/administration/gitaly/))
GitLab Rails | -
PostgreSQL | -
**Praefect** | The traffic manager making Git data highly available ([blog](https://about.gitlab.com/blog/2021/01/21/high-availability-git-storage-with-praefect/))
Prometheus | -
Redis | -
[**Sidekiq**](https://github.com/sidekiq/sidekiq) | GitLab uses Sidekiq as its background job processor

Look at the [Reference architectures](https://docs.gitlab.com/ee/administration/reference_architectures/) to understand when each component is needed.
