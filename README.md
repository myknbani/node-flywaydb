# node-flywaydb
NodeJs wrapper for [flywaydb cli](https://flywaydb.org/documentation/commandline/)

## Note on fork

As you can see from the header, this is a fork.  It downloads Flyway from the Google mirrors, since the original Maven repo is slow.  Won't submit a PR since I'm not sure if it's a location/Asia thing (the mirror URL contains Asia).

See [Maven download slow on SO](https://stackoverflow.com/questions/9974311/is-it-possible-to-speed-up-maven-artifacts-downloading) and
[Google mirrors on SO](https://stackoverflow.com/questions/61862887/how-to-use-google-mirror-for-maven-central-as-a-direct-link-to-download-an-artif).

## Motivation
I found myself wanting to use flyway on my build systems and dreading installing and maintaining the cli with all of the PATH requirements. This simple wrapper will download the latest Flyway cli on install and provide a hook for your package scripts.

## Example package script
```
"scripts": {
  "migrate": "flyway -c conf/flyway.js migrate"
}
```

See [Example config file for inspiration](sample/config.js)
