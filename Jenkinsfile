pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t dilipcse/service:v1 .'
            }
        }
        stage ("Push") {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'docker-id') {
                        sh 'docker push dilipcse/service:v1'
                }
        }
    }
}
}
}
