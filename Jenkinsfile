pipeline {
    agent any

    environment {
        EXAMPLE_ENV = credentials('fzrsahi')
    }

    stages {
        stage('example incorrect') {
            steps {
                sh("echo ${EXAMPLE_ENV}")
            }
        }

        stage('verify tooling') {
            steps {
                sh '''
            docker version
            docker info
            docker info
            docker compose version
            curl --version
                '''
            }
        }
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
