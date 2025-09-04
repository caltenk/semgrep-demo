pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/caltenk/semgrep-demo'
            }
        }

        stage('No-op') {
            steps {
                echo 'Repo checked out.'
            }
        }
    }
}
