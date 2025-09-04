pipeline {
    agent any

    environment {
        SEMGREP_APP_TOKEN = credentials('SEMGREP_APP_TOKEN')
        SEMGREP_PR_ID = "${env.CHANGE_ID}"
        PATH = "/var/jenkins_home/.local/bin:${env.PATH}"
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/caltenk/semgrep-demo'
            }
        }

        stage('Semgrep-Scan') {
            steps {
                sh 'semgrep ci'
            }
        }
    }
}
