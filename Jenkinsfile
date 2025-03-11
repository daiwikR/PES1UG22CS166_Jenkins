pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the C++ code...'
                // If you have a Makefile in main/, uncomment the following:
                sh 'make -C main'
            }
        }
        stage('Test') {
            steps {
                echo 'Running the executable...'
                // If your compiled file is "hello_exec" in main/:
                sh './main/hello_exec'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the build...'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
