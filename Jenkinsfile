pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -c PES1UG20CS405.cpp - error'
                sh 'g++ -o PES1UG20CS405 PES1UG20CS405.cpp'
                echo 'Build successful'
            }
        }
        stage('Test') {
            steps {
                sh './PES1UG20CS405'
                echo 'Test was successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy steps successful'
            }
        }
        
    }
    post{
       failure{
      echo 'Pipelined failed'
       }
    }
}
