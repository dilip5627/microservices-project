pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t dilipcse/currencyservice:v1 .'
            }
        }
        stage ("Push") {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'docker-id') {
                        sh 'docker push dilipcse/currencyservice:v1'
                }
        }
    }
}
}
}
