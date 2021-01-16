# Dev Containers

These are a collection of containers for languages that either VSCode does not have a template
or it is used to customize. A lot is borrowed from their templates.

All of the images use Alpine Linux.

## How to use

To use a container definition simply copy the folder to an empty directory and tell VSCode to reopen inside a container
it should pick up the Dockerfile and build it.

For example to use the elixir one in a new project do the following:

```
git clone https://github.com/sleepiejohn/devcontainers.git
cd devcontainers
cp devcontainers/elixir ~/myprojects/new_project -r
cd ~/myprojects/new_project
code .
```

Once inside the container you can do:

```
mix new .
```

Or your language scaffolding tool, and it should be all present on the root directory of the project along side with the `.devcontainer` folder.

## Changing versions

For now to change the version, change the base image on the [Dockerfile](https://github.com/sleepiejohn/devcontainers/blob/main/elixir/.devcontainer/Dockerfile#L1).
If necessity arises, it may be implemented as a series of `ARG` switches on the Dockerfile. 
