Mavenized Nexmo Java SDK
========================

The Nexmo Java SDK only comes as an Ant buildable git repostory - <https://github.com/Nexmo/nexmo-java> - and is not available from Maven Central.

This repository is a fork of that one - with the addition of a [`pom.xml`](pom.xml) file.

This pom wraps the Ant build process as per <http://stackoverflow.com/a/1456976> (and solves the javac issues as per <http://stackoverflow.com/a/31969775>.

The Ant build pulls its dependencies from the included [`lib`](lib) directory.

The pom here provides the corresponding Maven Central dependencies such that any downstream project can pull them in automatically.

The version specified in the pom is `1.6-SNAPSHOT` and corresponds in Maven speak to the version specified in the the Ant [`build.xml`](build.xml) file, i.e. `1-6-prerelease`.

Note: Nexmo don't seem to be bumping the version on changes to their repository and look to be in eternal prerelease state.

If the parent Nexmo repository gets updated in should be trivial to pull these changes and then:

* The dependencies in the pom may need to be updated to be kept in sync with those under `lib`.
* The version may need to be updated to match that in `build.xml`.

The project's original README can be found in [`README.txt`](README.txt).
