pipeline {
    agent { docker { image 'php' } }
    stages {
        stage('deploy') {
            steps {
                bat 'php --version'
            }
        }
    }
}
