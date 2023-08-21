pipeline {
    agent {
        label 'windows_node'
    }
    stages {
        
        stage('Clone code from github') {
            steps {
                    echo 'Checking out my code from github'
                    git credentialsId: '8fcad28a-cbcf-4b23-a576-daf918fe1e79', url: 'https://github.com/hesham98/Pipeline_Script.git'
            }
        }
        stage('build stage') {
            steps {
                    echo 'Building the checking out code'
                    bat 'Build.bat'
            }
        }
        stage('Unit test stage') {
            steps {
                    echo 'Running unit test on the checking out code'
                    bat 'Unit.bat'
            }
        }
        stage('Quality stage') {
            steps {
                    echo 'Verifying the quality'
                    bat 'Quality.bat'
            }
        }
        stage('Deploy stage') {
            steps {
                    echo 'Deploying the checking out code'
                    bat 'Deploy.bat'
            }
        }
    }
}