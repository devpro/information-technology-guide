# GitLab Runners

🌐 [docs](https://docs.gitlab.com/runner/)

## Executors

* [Docker](https://docs.gitlab.com/runner/executors/docker.html)
* [Docker Machine](https://docs.gitlab.com/runner/executors/docker_machine.html)
* [Docker Autoscaler](https://docs.gitlab.com/runner/executors/docker_autoscaler.html)
* [Instance](https://docs.gitlab.com/runner/executors/instance.html)
* [Kubernetes](https://docs.gitlab.com/runner/executors/kubernetes/index.html)
* [Shell](https://docs.gitlab.com/runner/executors/shell.html)
* [SSH](https://docs.gitlab.com/runner/executors/ssh.html)
* [VirtualBox](https://docs.gitlab.com/runner/executors/virtualbox.html)

## Debugging

## Local execution

Use Docker image (workaround found on [gitlab-runner issue#4275](https://gitlab.com/gitlab-org/gitlab-runner/-/issues/4275))

```bash
# creates local folder
mkdir -p .gitlab/runner/local

# displays help on a command
docker run --rm --name gitlab-runner -v /var/run/docker.sock:/var/run/docker.sock -v $PWD/.gitlab/runner/local/config:/etc/gitlab-runner -v $PWD:$PWD --workdir $PWD gitlab/gitlab-runner exec help

# executes shell on "build" job
docker run --rm --name gitlab-runner -v /var/run/docker.sock:/var/run/docker.sock -v $PWD/.gitlab/runner/local/config:/etc/gitlab-runner -v $PWD:$PWD --workdir $PWD gitlab/gitlab-runner exec shell build
```

Warning: Includes are not supported unfortunately ([Issue #2797](https://gitlab.com/gitlab-org/gitlab-runner/-/issues/2797), alternative with [firecow/gitlab-ci-local](https://github.com/firecow/gitlab-ci-local))
