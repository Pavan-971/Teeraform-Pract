pipeline {
  agent any
  
  environment {
    
    
    AWS_ACCESS_KEY_ID = "g!GvRUtcX8R&"
    AWS_SECRET_ACCESS_KEY = "AKIAZCNSO4VDGOTYUAVP"
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
