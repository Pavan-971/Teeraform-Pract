pipeline {
  agent any
  parameters {
    password (name: 'AWS_ACCESS_KEY_ID', defaultValue: "AKIAZCNSO4VDNWPU7HGO")
    password (name: 'AWS_SECRET_ACCESS_KEY', defaultValue: "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")
  }
  
  environment {
    
    
    AWS_ACCESS_KEY_ID = "${params.AWS_ACCESS_KEY_ID}"
    AWS_SECRET_ACCESS_KEY = "${params.AWS_SECRET_ACCESS_KEY}"
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
