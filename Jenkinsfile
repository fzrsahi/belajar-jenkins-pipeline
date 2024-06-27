pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('hello 2') {
            steps {
                echo 'Hello World 2'
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
