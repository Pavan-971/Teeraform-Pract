def awsCredentials = [[$class: 'AmazonWebServicesCredentialsBinding', credentialsId: 'aws-personal']]

pipeline {
  agent any
  
  options {
 
  withCredentials(awsCredentials)
}
 
  stages {
    stage('Terraform Init') {
      steps {
        sh "terraform init "
      }
    }
    stage('Terraform Plan') {
      steps {
        sh "terraform plan -out=tfplan -input=false "
       
      }
    }
    stage('Terraform Apply') {
      steps {
        
        sh "terraform apply -input=false tfplan" 
        sh "echo hi......hhhhhhggggg."
        
      }
    }
    
  }
}
