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
                    sh "docker build -t flask-app ."
                    sh "docker image ls"
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
                sh "docker run -p 5000:5000 --name flask-app -d flask-app"
                echo 'Deploying....'
            }
        }
    }
}