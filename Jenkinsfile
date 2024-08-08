pipeline {
    agent any

    environtment {
        EXAMPLE_ENV = credentials('awikwok===')
    }

    stages {
        stage('example incorrect') {
            steps {
                sh("echo ${EXAMPLE_ENV}")
            }
        }

        stage('example correct') {
            steps {
                sh('echo $EXAMPLE_ENV')
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
