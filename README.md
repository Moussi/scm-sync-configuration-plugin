Jenkins SCM Sync Configuration Plugin
=====================

Read more: [https://wiki.jenkins-ci.org/display/JENKINS/SCM+Sync+configuration+plugin](https://wiki.jenkins-ci.org/display/JENKINS/SCM+Sync+configuration+plugin)

# Building

To build the plugin, you'll need maven (`brew install maven`). Once maven is installed, simply run:

```
mvn install
```

This will build the image and run the tests. The configuration is found at `./target/scm-sync-configuration.hpi`
