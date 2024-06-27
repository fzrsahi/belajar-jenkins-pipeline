pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build'
            }
        }
        stage('Test') {
            steps {
                echo 'Test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy'
            }
        }
        stage('Umar') {
            steps {
                echo 'Anjay'
            }
        }
    }

    post {
        always {
            echo 'always'
        }
        success {
            echo 'success'
        }
        failure {
            echo 'fail'
        }
        cleanup {
            echo 'dont care fail or success'
        }
    }
}
