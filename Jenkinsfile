pipeline {
    agent any
    environment {
        JAVA_HOME = "/usr/lib/jvm/java-17-openjdk-amd64/"
        M2_HOME = "/opt/apache-maven-3.8.7"
        PATH = "$M2_HOME/bin:$PATH"
    }
    stages {
        stage('Checkout') {
            steps {
                sshagent(credentials: ['jenkins-key']) {
                    git url: 'git@github.com:ferielyahyaoui/gestion_spring.git', branch: 'main'
                }
            }
        }

        stage('Compile') {
            steps {
                sh 'mvn clean compile'
            }
        }
    }
}
