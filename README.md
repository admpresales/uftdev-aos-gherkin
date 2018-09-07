# leanft-gherkin
Since the LeanFT jar files are not part of a public maven repo, maven projects will fail to grab the required jars.  This can be solved by connecting to a private maven repo or by adding the jar files to the local maven repo cache manually.  More information can befound visiting https://admhelp.microfocus.com/leanft/en/14.50/HelpCenter/Content/HowTo/prerequ-maven.htm

Note: The Selenium jars are not used as part of this project but can be added using normal maven practices by adding the dependency to your pom file.  The publc definition can be found https://search.maven.org/search?q=a:leanft-selenium-java-sdk

The below assume you have performed a default installation of UFT Pro (LeanFT).  You would just need to adjust the path to the jar files where appropriate.  As a note for future use, change the version number to match the version of LeanFT that you are using.

# Mac
The following maven goals were used to add the 14.50.0 lft libraries to the local maven cache (.m2) for IntelliJ 2017.3 on a Apple Mac
The lines below were executed using IntelliJ UI.

install:install-file -Dfile="/Applications/LeanFT/sdk/Java/com.hp.lft.sdk-standalone.jar" -DgroupId=com.hp.lft -DartifactId=sdk -Dversion=14.50.0 -Dpackaging=jar

install:install-file -Dfile="/Applications/LeanFT/sdk/Java/com.hp.lft.sdk-javadoc.jar" -DgroupId=com.hp.lft -DartifactId=sdk -Dclassifier=javadoc -Dversion=14.50.0 -Dpackaging=jar

install:install-file -Dfile="/Applications/LeanFT/sdk/Java/com.hp.lft.unittesting.jar" -DgroupId=com.hp.lft -DartifactId=unittesting -Dversion=14.50.0 -Dpackaging=jar

install:install-file -Dfile="/Applications/LeanFT/sdk/Java/com.hp.lft.verifications.jar" -DgroupId=com.hp.lft -DartifactId=verifications -Dversion=14.50.0 -Dpackaging=jar

install:install-file -Dfile="/Applications/LeanFT/sdk/Java/com.hp.lft.report.jar" -DgroupId=com.hp.lft -DartifactId=report -Dversion=14.50.0 -Dpackaging=jar

If maven is installed as a standalone (rather than just a plugin ot IntelliJ) the following should work, though not verified *or* use the terminal screen in IntelliJ and execute the below commands.  Keep in mind it is assuming default installation of LFT 14.0

mvn install:install-file -Dfile="/Applications/LeanFT/sdk/Java/com.hp.lft.sdk-standalone.jar" -DgroupId=com.hp.lft -DartifactId=sdk -Dversion=14.50.0 -Dpackaging=jar

mvn install:install-file -Dfile="/Applications/LeanFT/sdk/Java/com.hp.lft.sdk-javadoc.jar" -DgroupId=com.hp.lft -DartifactId=sdk -Dclassifier=javadoc -Dversion=14.50.0 -Dpackaging=jar

mvn install:install-file -Dfile="/Applications/LeanFT/sdk/Java/com.hp.lft.unittesting.jar" -DgroupId=com.hp.lft -DartifactId=unittesting -Dversion=14.50.0 -Dpackaging=jar

mvn install:install-file -Dfile="/Applications/LeanFT/sdk/Java/com.hp.lft.verifications.jar" -DgroupId=com.hp.lft -DartifactId=verifications -Dversion=14.50.0 -Dpackaging=jar

mvn install:install-file -Dfile="/Applications/LeanFT/sdk/Java/com.hp.lft.report.jar" -DgroupId=com.hp.lft -DartifactId=report -Dversion=14.50.0 -Dpackaging=jar

mvn install:install-file -Dfile="/Applications/LeanFT/sdk/Java/com.hp.lft.reportbuilder-standalone.jar" -DgroupId=com.hp.lft -DartifactId=reportbuilder -Dversion=14.50.0 -Dpackaging=jar

# Ubuntu/Linux
/usr/bin/mvn install:install-file -Dfile=/opt/leanft/sdk/Java/com.hp.lft.sdk-standalone.jar -DgroupId=com.hp.lft -DartifactId=sdk -Dversion=14.50.0 -Dpackaging=jar

/usr/bin/mvn install:install-file -Dfile=/opt/leanft/sdk/Java/com.hp.lft.sdk-javadoc.jar -DgroupId=com.hp.lft -DartifactId=sdk -Dclassifier=javadoc -Dversion=14.50.0 -Dpackaging=jar

/usr/bin/mvn install:install-file -Dfile=/opt/leanft/sdk/Java/com.hp.lft.unittesting.jar -DgroupId=com.hp.lft -DartifactId=unittesting -Dversion=14.50.0 -Dpackaging=jar

/usr/bin/mvn install:install-file -Dfile=/opt/leanft/sdk/Java/com.hp.lft.verifications.jar -DgroupId=com.hp.lft -DartifactId=verifications -Dversion=14.50.0 -Dpackaging=jar

/usr/bin/mvn install:install-file -Dfile=/opt/leanft/sdk/Java/com.hp.lft.report.jar -DgroupId=com.hp.lft -DartifactId=report -Dversion=14.50.0 -Dpackaging=jar

/usr/bin/mvn install:install-file -Dfile=/opt/leanft/sdk/Java/com.hp.lft.reportbuilder-standalone.jar -DgroupId=com.hp.lft -DartifactId=reportbuilder -Dversion=14.50.0 -Dpackaging=jar

# Windows
If on a windows machine, you should alter the path of where the jar file is located.
Below can be used for Windows LFT installation assuming it is for LFT 14 with the default installation of LFT

mvn install:install-file -Dfile="C:\Program Files (x86)\HP\Unified Functional Testing\SDK\Java\com.hp.lft.sdk-standalone.jar" -DgroupId=com.hp.lft -DartifactId=sdk -Dversion=14.50.0 -Dpackaging=jar

mvn install:install-file -Dfile="C:\Program Files (x86)\HP\Unified Functional Testing\SDK\Java\com.hp.lft.sdk-javadoc.jar" -DgroupId=com.hp.lft -DartifactId=sdk -Dclassifier=javadoc -Dversion=14.50.0 -Dpackaging=jar

mvn install:install-file -Dfile="C:\Program Files (x86)\HP\Unified Functional Testing\SDK\Java\com.hp.lft.unittesting.jar" -DgroupId=com.hp.lft -DartifactId=unittesting -Dversion=14.50.0 -Dpackaging=jar

mvn install:install-file -Dfile="C:\Program Files (x86)\HP\Unified Functional Testing\SDK\Java\com.hp.lft.verifications.jar" -DgroupId=com.hp.lft -DartifactId=verifications -Dversion=14.50.0 -Dpackaging=jar

mvn install:install-file -Dfile="C:\Program Files (x86)\HP\Unified Functional Testing\SDK\Java\com.hp.lft.report.jar" -DgroupId=com.hp.lft -DartifactId=report -Dversion=14.50.0 -Dpackaging=jar

mvn install:install-file -Dfile="C:\Program Files (x86)\HP\Unified Functional Testing\SDK\Java\com.hp.lft.reportbuilder-standalone.jar" -DgroupId=com.hp.lft -DartifactId=reportbuilder -Dversion=14.50.0 -Dpackaging=jar

# Process to change the test

From a machine connected to the Micro Focus network perform the following:

1. git clone https://github.hpe.com/admpresales/leanft-gherkin
1. git checkout -b \<mybranchname\>
1. Make desired changes
1. git commit
1. git push
1. Then from https://github.hpe.com/admpresales/leanft-gherkin perform a pull request on the branch
