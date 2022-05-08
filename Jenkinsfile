pipeline {
    agent any

    stages {
        stage('Process Data') {
            steps {
                sh "pwd"
                dir('preprocessing'){
                    sh "python3 preprocessing.py"
                }
                echo 'Processing Data'
            }
        }        
        stage('Build') {
            steps {
                sh "pwd"
                dir('app'){
                    sh "sudo docker build -t flask-app ."
                    sh "sudo docker image ls"
                }                
                echo 'Building docker image'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}