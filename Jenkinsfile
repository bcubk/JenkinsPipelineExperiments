node() {
    stage("Checkout") {
        checkout scm
    }

    stage("Build") {
        def mvnHome = tool 'maven-3.3.9'
        sh "${mvnHome}/bin/mvn clean install"
    }
}