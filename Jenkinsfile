pipeline {
  agent any
  
  environment {
    
    
    AWS_ACCESS_KEY_ID = "AKIAZCNSO4VDGOTYUAVP"
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
        sh "terraform plan "
      }
    }
    stage('Terraform Apply') {
      steps {
        
        sh "terraform apply -auto-approve "
      }
    }
    
  }
}
