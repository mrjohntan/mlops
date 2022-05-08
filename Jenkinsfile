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