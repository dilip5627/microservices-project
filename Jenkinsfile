pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t dilipcse/emailservice:v1 .'
            }
        }
        stage ("Push") {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'docker-id') {
                        sh 'docker push dilipcse/emailservice:v1'
                }
        }
    }
}
}
}
