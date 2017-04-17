node() {
    stage("Checkout") {
        checkout scm
    }

    def mvnHome = tool 'maven-3.5.0'
    stage("Build") {
        sh "${mvnHome}/bin/mvn clean install"
    }

    stage("Sonar Quality Gate") {
        withSonarQubeEnv('Sonar') {
            sh "${mvnHome}/bin/mvn sonar:sonar"
        }
    }
}