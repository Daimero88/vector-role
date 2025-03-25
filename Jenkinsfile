pipeline {
    agent {
        label 'jenkins-agent'
    }
    stages {
        stage ('Copy Git repo') {
            steps {
                sh 'sudo -i'
                sh 'git clone https://github.com/Daimero88/vector-role.git'
            }
        }
        stage ('Run molecule test') {
            steps {
                dir('vector-role') {
                    sh 'molecule test'
                }
            }
        }
    }
}
