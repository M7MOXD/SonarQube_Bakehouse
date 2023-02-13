pipeline {
    agent { label 'master' }
    stages {
        stage('SonarQube') {
            steps {
                script {
                    def scannerHome = tool 'sonarqube';
                    withSonarQubeEnv('sonarqube_server') {
                        sh "${scannerHome}/bin/sonar-scanner"
                    }

                }
            }
        }
    }
}