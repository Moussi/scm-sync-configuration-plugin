Jenkins SCM Sync Configuration Plugin

This repository is a fork of the mainline plugin, which apperas to be unmaintained!

=====================

Read more: [https://wiki.jenkins-ci.org/display/JENKINS/SCM+Sync+configuration+plugin](https://wiki.jenkins-ci.org/display/JENKINS/SCM+Sync+configuration+plugin)

# Building

To build the plugin, you'll need maven (`brew install maven`). Once maven is installed, simply run:

```
mvn install
```

This will build the image and run the tests. The configuration is found at `./target/scm-sync-configuration.hpi`

Thanks to hybris/scm-sync-configuration-plugin for his PR for adding git branch on scm sync plugin 
https://github.com/jenkinsci/scm-sync-configuration-plugin/pull/23/commits
