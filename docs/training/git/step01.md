# Step 1

In this step, we are going to look at the environment and see how to view & update the configuration.

* Display the git client version:

`git version`{{execute}}

* Look at the available git commands:

`git help`{{execute}}

* List all configuration:

`git config -l`{{execute}}

* Set your identity (you can update it):

`git config --global user.name "John Doe"`{{copy}}

`git config --global user.email johndoe@example.com`{{copy}}

* Set default branch name:

`git config --global init.defaultBranch main`{{execute}}

* List at the updated configuration:

`git config -l`{{execute}}

* You can also look at one configuration in particular:

`git config user.name`{{execute}}

* Finally look at where it is stored

`more $HOME/.gitconfig`{{execute}}

References: [Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git), [First-Time Git Setup](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup), [Getting Help](https://git-scm.com/book/en/v2/Getting-Started-Getting-Help)
