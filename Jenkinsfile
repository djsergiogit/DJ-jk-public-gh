pipeline {
    agent any

    stages {
        stage('Clonning Git Repository by Sergio') {
            steps {
                git branch: 'main', url: 'https://github.com/djsergiogit/DJ-jk-public-gh.git'
            }
        }
        stage('Building Image by Sergio') {
            steps {
                sh 'docker build -t webapp:${BUILD_NUMBER} .'
            }
        }
        stage('Deploy Application of Sergio') {
            steps {
                sh 'docker run --rm -d -p 3000:3000 --name webapp_ctr webapp:${BUILD_NUMBER}'
            }
        }
    }
}   
