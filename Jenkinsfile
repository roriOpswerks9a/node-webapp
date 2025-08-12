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

