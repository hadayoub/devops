pipeline {
    agent any
    options{
    buildDiscarder(logRotator(numToKeepStr:'5'))
    }
    stages {
        stage('scan') {
            steps {
                withSonarQubeEnv(installationName: 'sq1'){
                    sh './mvnw clean org.sonarsource.scanner.maven:sonar-maven-plugin:3.9.0.2155:sonar'
                }
            }
        }
    
    }
}
