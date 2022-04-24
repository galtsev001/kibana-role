pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
                dir('kibana-role') {
                    git credentialsId: 'github_galtsev001', url: 'https://github.com/galtsev001/kibana-role.git'
                }
            }
        }
        stage('install requirements') {
            steps {
                dir('ansible-role-kibana') {
                    sh 'pip3 install -r requirements.txt'
                }
            }
        }
        stage('run molecule') {
            steps {
                dir('kibana-role') {
                    sh 'molecule test'
                }
            }
        }
    }
}