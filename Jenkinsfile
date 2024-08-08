pipeline {
    agent any
    environment {
        AWS_ACCESS_KEY_ID     = credentials('fzrsahi')
    }
    stages {
        stage('Example stage 1') {
            steps {
                echo 'Hello $AWS_ACCESS_KEY_ID'
            }
        }
    }
}
