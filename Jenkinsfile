pipeline {
    agent any
    stages {
        stage('Clone Repo') {
            steps {
                git(
                    url: 'https://github.com/roriOpswerks9a/node-webapp.git',
                    branch: 'main',
                    credentialsId: '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'
                )
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run App') {
            steps {
                sh 'nohup npm start &'
            }
        }
    }
}
