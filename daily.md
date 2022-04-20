
## We can pass user-defined properties to gradlew and build.gradle file can receive the value.

> def buildChannel = project.getProperties().get("buildChannel")

> gradlew assemble assembleAndroidTest -PbuildChannel=jenkins


The passing user-defined properties [README.md](https://stackoverflow.com/questions/47051593/gradle-command-line-arguments-to-override-properties-in-build-gradle)