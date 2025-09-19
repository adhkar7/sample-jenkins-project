pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/adhkar7/sample-jenkins-project.git'
            }
        }
        stage('Build') {
            steps {
                sh './hello.sh'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Running tests... (fake test passed ✅)"'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying application... 🚀"'
            }
        }
    }
}
