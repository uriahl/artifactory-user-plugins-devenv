How to configure artifactory plugin development

go to the gradle.properties and set the artifactoryVersion to the version you are using  
go to the gradle.properties and paste in your download link for artifactory.  
link in plugins to be worked in in the etc/plugins directory (see readme there)

All of the configuration happens with gradle tasks:

To set up your ide type:  ./gradlew idea (or eclipse)
To download and configure artifactory: ./gradlew prepareArtPro
To start artifactory: ./gradlew startArtPro

Then you can run the tests present in 'artifactory-plugin/src/test/groovy/org/jfrog/vcac/test/' using your IDE.

To stop artifactory: ./gradlew stopArtPro

To erase all artifactory storages: ./gradlew cleanArtPro

Artifactory will be configured with the artifactory pro license present in the etc folder,
a representative set of repositories, and will poll the plugins directory for updates every 10 seconds.


