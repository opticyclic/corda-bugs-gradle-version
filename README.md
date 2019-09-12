# Corda Bugs - Gradle Version

This demonstrates a bug in Corda dependent on the version of gradle used.

The master branch shows the error.

The `4.4.1` branch shows the same code but working.

The only difference is the gradle version.

You can either switch to the other branch to test or you can change the gradle version in master.

## Commands 

Show gradle version:

    ./gradlew --version

Clean the working copy:

    ./gradlew clean;rm -rf workflows/logs/;rm -rf .gradle

Run the tests:

    ./gradlew :workflows:integrationTest --tests "com.template.ExampleDriverBasedTest"

Downgrade to an earlier version of gradle and repeat:

    ./gradlew wrapper --gradle-version 4.4.1
    ./gradlew --version
    ./gradlew clean;rm -rf workflows/logs/;rm -rf .gradle
    ./gradlew :workflows:integrationTest --tests "com.template.ExampleDriverBasedTest"
 