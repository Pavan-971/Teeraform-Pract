pipeline {
  agent any
  
  environment {
    
    
    AWS_ACCESS_KEY_ID = "AKIAZCNSO4VDHIQYMPFM"
    AWS_SECRET_ACCESS_KEY = "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"
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
      }
    }
    
  }
}
