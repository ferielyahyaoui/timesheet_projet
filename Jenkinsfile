pipeline {

 agent any

 environment {
         JAVA_HOME = "/usr/lib/jvm/java-17-openjdk-amd64/"
         M2_HOME = "/opt/apache-maven-3.6.3"
         PATH = "$M2_HOME/bin:$PATH"

     }

 stages {

 stage('GIT') {

           steps {

               git branch: 'main',

               url: 'https://github.com/ferielyahyaoui/timesheet_projet.git'

          }

     }

 stage ('Compile Stage') {

    steps {

    sh 'mvn clean compile'

    }

 }

}


}
