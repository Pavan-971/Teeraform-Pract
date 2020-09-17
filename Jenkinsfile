pipeline {
  agent any
  
  environment {
    
    TF_IN_AUTOMATION = 'true'
    AWS_ACCESS_KEY_ID = "AKIAZCNSO4VDBMDMHQN3"
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
        
        sh "terraform apply -auto-approve -input=false "
      }
    }
    
  }
}
