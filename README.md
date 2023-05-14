# Repo tool Manifest
Repo is a tool that we use to manage multiple git repositories, it is not a built-in git command. It is a wrapper around git that provides additional functionality that is useful for working with multiple repositories.

It helps me learning and investigate multiple repos for specific topic, group those repos in a single manifest and checkout them in a single command.

## Install git-repo tool
Many distros include repo, so you might be able to install from there.

### Debian/Ubuntu.
```
$ sudo apt-get install repo
```

#### Manual install
$ sudo emerge dev-vcs/repo
You can install it manually as well as it's a single script.

```
mkdir -p ~/.bin
PATH="${HOME}/.bin:${PATH}"
curl https://storage.googleapis.com/git-repo-downloads/repo > ~/.bin/repo
chmod a+rx ~/.bin/repo
```

## Use this manifest
The following commands will allow you to checkout a working set of repositories to build the system:

# Use a work directory for your project
```
$ mkdir my_project_name
$ cd my_project_name/
```
Next checkout repositories using the repo-manifest:

```
repo init -u ssh://your-git-host/path/to/repo-manifest"
repo sync
```

## Why repo ?
Most modern systems/projects are divided into several Git repositories, each of them containing a specific set of files for a specific function.

To work together well, these repositories must be checked out at a very specific revision, which is compatible with each other’s repository specific revision. This can be a tedious task to do and require manual repetition, and that’s where repo comes in handy.

## References
[Git-Repo tool](https://gerrit.googlesource.com/git-repo/)