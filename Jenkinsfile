pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checkout source code'
            }
        }

        stage('Run Robot Tests') {
            steps {
                sh 'robot tests/Lab8.robot'
            }
        }
    }
}
