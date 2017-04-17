node() {
    stage("Checkout") {
        checkout scm
    }

    stage("Build") {
        def mvnHome = tool 'maven-3.5.0'
        sh "${mvnHome}/bin/mvn clean install"
    }
}