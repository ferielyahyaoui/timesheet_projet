pipeline {
    agent any
  environment {
        JAVA_HOME = "/usr/lib/jvm/java-17-openjdk-amd64/"
        M2_HOME = "/usr/share/maven"  // Mise à jour du chemin de Maven
        PATH = "$M2_HOME/bin:$PATH"
    }

    stages {
        stage('Hello Test') {
            steps {
                echo ' hello feryal '
            }
        }

        stage('Git Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/ferielyahyaoui/timesheet_projet.git',
                    credentialsId: 'jenkins-key'
            }
        }

        stage('Clean compile') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Sonar Analysis') {
			steps {
				withSonarQubeEnv('sq1') {
					sh 'mvn sonar:sonar'
                        }
                    }
                }
       

       
    }
}
