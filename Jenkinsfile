pipeline {
    agent any

    tools {
        jdk 'JAVA_HOME' 
        maven 'M2_HOME'
    }

    stages {
        stage('GIT') {
            steps {
                sshagent(credentials: ['jenkins-key']) {
                    git url: 'git@github.com:ferielyahyaoui/timesheet_projet.git', branch: 'main'
                }
            }
        }

        stage ('Compile Stage') {
            steps {
                sh 'mvn clean compile'
            }
        }
    }
}
