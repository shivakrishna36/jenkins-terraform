pipeline {
   agent any
      tools {
        maven 'maven3.6.3'
        jdk 'jdk8'
        terraform 'terraform'

    	}
   stages {
      
      stage('Hello') {
         steps {
             bat 'terraform --version'
             echo 'Hello World'
         }
      }
      
      
       stage('check cmd') {
            steps {
               dir('/terraform') {
                  bat 'terraform init'
                  bat 'terraform apply -auto-approve'
                  }
               }
            }
         
      
      }
}
