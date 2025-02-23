pipeline {

 agent any

 tools {jdk 'JAVA_HOME’, maven 'M2_HOME'}

 stages {

 stage('GIT') {

           steps {

               git branch: 'master',

               url: 'git@github.com:ferielyahyaoui/timesheet_projet.git'

          }

     }

 stage ('Compile Stage') {

 steps {

 sh 'mvn clean compile'

 }

 }

 }

}
