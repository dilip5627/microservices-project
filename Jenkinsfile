pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t dilipcse/checkoutservice:v1 .'
            }
        }
        stage ("Push") {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'docker-id') {
                        sh 'docker push dilipcse/checkoutservice:v1'
                }
        }
    }
}
}
}
