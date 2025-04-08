pipeline {
    agent any

    stages {
        stage('build docker image') {
            steps {
                sh "docker build -t meher27/recommendationservice:v1 ."
            }
        }
        stage ("docker-push") {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'docker') {
                    sh "docker push meher27/recommendationservice:v1"
}
                }
            }
        }
    }
}
