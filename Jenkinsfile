pipeline {
   agent any

   stages {
      stage('Hello') {
         steps {
             def tfHome = tool name: 'terraform', type: 'com.cloudbees.jenkins.plugins.customtools.CustomTool'
             env.Path = "${tfHome};${env.Path}"
             bat 'terraform --version'
             echo 'Hello World'
         }
      }
   }
}
