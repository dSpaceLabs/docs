Standards
=========

dSpace Labs LLC standards when it comes to coding and general development
practices. Most of this document is what I consider to by guidelines. Guidelines
are suggestions that you should comply with to make development smoother. If
there is something here that you do not agree with, fork and submit a pull
request.

## dSpace Labs LLC Branding Guidelines

The name MUST be written as `dSpace Labs LLC` with a lowercase 'd'. This is the
fully qualified legal name of this organization. When coding, this name SHOULD
confirm to the languages best practices. For example, all PHP code SHOULD be
under the namespace `Dspace`. For example `Dspace\Component\User`.

Yes: `dSpace Labs LLC`

No: `Dspace Labs LLC`

No: `dSpace Labs`

## IRC Channels

- [#dspacelabs](irc://chat.freenode.net/dspacelabs)

## General Workflow Guidelines

@todo What are the tools that are used and how to use the tools.

### [GitHub](https://github.com/)

- Preferred hosting for all git repositories.
- Disabled Issues and Wiki

@todo release process

### [Pivotal Tracker](https://pivotaltracker.com/)

- Preferred issue tracker and project management

@todo Look into replacing with task warrior

### [Travis CI](https://travis-ci.org/)

- Preferred continuous integration and deployment
- Notifications should be sent to #dspacelabs

### [Heroku](https://heroku.com/)

- Sites deployed here

### AWS

- Use some services such as S3 for storage

## Git Guidelines

The recommended work flow for working with any project, is to fork the project
and submit pull requests back to the main branch. Through out this guideline
there will be references to `upstream` instead of `origin`. If you are unsure of
how to setup an "upstream" remote repository. Just execute the command:

```shell
$ git remote add upstream https://github.com/dspacelabs/REPOSITORY.git
```

### Branches

- *master* is a branch that SHOULD always be stable enough to ship. The
exception here is for libraries. The *master* branch for a library is the
current development version. For a stable version, tags SHOULD be used.
- *version* branches are named after the version. For example, version 1.4.0 would
be found on branch *1.x*. These branches are used mostly for libraries. These
branches provide a way to allow bug fixes and on going maintenance without
breaking too many things.

### Branching

#### Branching for Features

Feature branches are cut from the current *master* branch and named after the
card number in Pivotal Tracker. Examples include: `story-84896650`.

```shell
# Make sure you are on master branch
$ git checkout master

# Make sure you have the latest and greatest
$ git pull upstream master --rebase --prune

# Cut a new branch off master
$ git checkout -b story-84896650
```

Alternative Method

```shell
# Make sure upstream/master is up to date
$ git fetch upstream master

# Create your feature branch
$ git checkout -b story-84896650 upstream/master
```

#### Branching for Hot Fixes

@todo explain this process

#### Bugs

See Feature Branches. Most bugs will be documented and a story written for such
a bug.

### Committing Changes

@todo explain commit messages

### Merges, Rebases, and Pull Requests, OH MY!

@todo explain the who, what, why, where, and when

### Tagging

@todo

### References

These helped shaped the ideas here.

- https://github.com/agis-/git-style-guide
- http://nvie.com/posts/a-successful-git-branching-model/
- http://symfony.com/doc/master/contributing/code/git.html
- https://help.github.com/articles/configuring-a-remote-for-a-fork/

## README.md Guidelines

@todo

## CHANGELOG.md Guidelines

@todo

### References

- http://keepachangelog.com/

## CONTRIBUTING.md Guidelines

@todo

## License Guidelines

@todo add a few more details

- Prefer MIT for projects
- Creative Commons for documents

## Version Guidelines

- Use Semantic Versioning

### References

- http://semver.org/

## PHP Guidelines

- Follow PSR standards.
- prefer symfony 2 for large apps
- prefer silex for small apps like api only tools

### References

- http://www.php-fig.org/psr/psr-1/
- http://www.php-fig.org/psr/psr-2/
- http://symfony.com/
- http://silex.sensiolabs.org/

## Restful API Guidelines

@todo

### References

- http://www.vinaysahni.com/best-practices-for-a-pragmatic-restful-api

## General References that I'm not sure where to put yet

- http://12factor.net/
- http://speaking.io/
