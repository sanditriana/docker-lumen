pipeline {
    agent any
    stages {
        stage('Build and deploy for dev') {
            when {
                branch 'dev' 
            }
            steps {
                sh 'rsync -av . root@192.168.1.202:/var/www/ds-core-dev/'
                sh 'ssh root@192.168.1.202 "cd /var/www/ds-core-dev/;docker exec ds-core-php-fpm composer update"'
                sh 'echo "success1"'
            }
        }
        stage('Build and deploy for staging') {
            when {
                branch 'staging' 
            }
            steps {
                sh 'echo "success for staging"'
            }
        }
        stage('Build and deploy for prod') {
            when {
                branch 'prod' 
            }
            steps {
                sh 'echo "success for prod"'
            }
        }
    }
}
