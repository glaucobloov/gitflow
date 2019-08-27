gitflow
========

The `development` branch the default branch where most of the work will happen, and the master branch keeps track of production-ready code.

## Feature branches

git-flow makes it easy to work on multiple features at the same time by using feature branches. To start one, use feature start with the name of your new feature.

## Versioned releases

If you need tagged and versioned releases, you can use git-flow’s release branches to start a new branch when you’re ready to deploy a new version to production.

## Hotfixing production code

Because you keep your master branch always in sync with the code that’s on production, you’ll be able to quickly fix any issues on production.

### Creating feature/release/hotfix/support branches

* To list/start/finish feature branches, use:

      Start: development – create branch >> feature/login 
      Done: feature/login – merge >> develop
  
  For feature branches, the `<base>` arg must be a commit on `development`.

* To list/start/finish release branches, use:

      Start: development – merge >> release
      Done: release – create tag >> release- v1.0.1-b10
  
  For release branches, the `<base>` arg must be a commit on `development`.
  
* To list/start/finish hotfix branches, use:

      Start: master – create branch >> hotfix/login 
      Update development: hotfix/login – merge >> development 
      Done: development – merge >> master
  
  For hotfix branches, the `<base>` arg must be a commit on `master`.
