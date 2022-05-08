pipeline {
    agent any

    stages {
        stage('Process Data') {
            steps {
                sh "pwd"
                dir(preprocessing){
                    sh "py preprocessing.py"
                }
                echo 'Processing Data'
            }
        }        
        stage('Build') {
            steps {
                echo 'Building..'
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