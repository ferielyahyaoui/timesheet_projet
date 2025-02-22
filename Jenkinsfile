pipeline {
    agent any
    stages {
        stage('GIT') {
            steps {
                sshagent(credentials: ['jenkins-key']) {
                    git url: 'git@github.com:ferielyahyaoui/timesheet.git', branch: 'main'
                }
            }
        }
    }
}
