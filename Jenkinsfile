pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/vantoantg/jenkins_002.git'
            }
        }
        stage('SSH to toannguyen') {
            steps {
                sshagent(['ssh-toannguyen-ubuntu-128']) {
                    sh 'ssh -o StrictHostKeyChecking=no -l toannguyen 192.168.200.128 touch tesssst.txt && touch tesssst222.txt'
                }
            }
        }
    }
}