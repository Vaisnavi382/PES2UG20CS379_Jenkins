pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES2UG20CS379-1 error.cpp'
                echo 'Build Successful'
            }
        }
        stage('Test') {
            steps {
                sh './PES2UG20CS379-1'
            }
        }
        stage('Deploy'){
            steps{
                sh 'mvn deploy'
                echo 'Deployment Successful'
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline completed'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
