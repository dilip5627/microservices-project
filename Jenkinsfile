pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t dilipcse/adservice:v1 .'
            }
        }
        stage ("Push") {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'docker-id') {
                        sh 'docker push dilipcse/adservice:v1'
                }
        }
    }
}
}
}
