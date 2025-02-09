# GitLab Platform Architecture

## Components

### Overview

Name           | Role
---------------|---------------------------------------------------------------------------------------------------------------------------
**Gitaly**     | High-level RPC access to Git repositories
**Geo**        | solution for widely distributed development teams and for providing a warm-standby as part of a disaster recovery strategy
GitLab Rails   | -
**PostgreSQL** | Only supported database
**Praefect**   | Traffic manager making Git data highly available
Prometheus     | -
Redis          | -
**Sidekiq**    | Background job processor

### Gitaly

> Gitaly is a Git RPC service for handling all the Git calls made by GitLab.

🌐 [gitlab-org/gitaly](https://gitlab.com/gitlab-org/gitaly)

📝 [docs.gitlab.com/administration/gitaly](https://docs.gitlab.com/ee/administration/gitaly/)

### Praefect

> Gitaly storage node traffic manager to provide a Gitaly Cluster.
> Praefect inspects the request and tries to route it to the right Gitaly backend, checks that Gitaly is up, makes sure the copies of your data are up to date, and so on.

📝 [about.gitlab.com/blog/2021/01/21](https://about.gitlab.com/blog/2021/01/21/high-availability-git-storage-with-praefect/)

### Sidekiq

> Simple, efficient background jobs for Ruby.

🌐 [sidekiq/sidekiq](https://github.com/sidekiq/sidekiq)

📝 [docs.gitlab.com/development/sidekiq](https://docs.gitlab.com/ee/development/sidekiq/)

### Geo

> Geo is the solution for widely distributed development teams and for providing a warm-standby as part of a disaster recovery strategy.
> Geo is not an out of the box HA solution.

📝 [docs.gitlab.com/administration/geo](https://docs.gitlab.com/ee/administration/geo/index.html), [How we built GitLab Geo](https://about.gitlab.com/blog/2018/09/14/how-we-built-gitlab-geo/),
[Geo glossary](https://docs.gitlab.com/ee/administration/geo/glossary.html)

### PostgreSQL

> PostgreSQL is the only supported database and is bundled with the Linux package.
> You can also use an external PostgreSQL database which must be tuned correctly.

📝 [docs.gitlab.com/install/requirements](https://docs.gitlab.com/ee/install/requirements.html#postgresql)
