pipeline {
    agent { label 'linux-node' }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    credentialsId: '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',
                    url: 'https://github.com/roriOpswerks9a/node-webapp.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('node-webapp-image')
                }
            }
        }

        stage('Run Container') {
            steps {
                script {
                    docker.image('node-webapp-image').run('-d -p 3000:3000')
                }
            }
        }
    }
}
