pipeline {
  parameters {
    password (name: 'AKIAZCNSO4VDBMDMHQN3')
    password (name: 'i8Up1jhU+8IVx6Mf4CPUces+KptdpW/sSWYzR/hD')
  }
  environment {
    
    TF_IN_AUTOMATION = 'true'
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
        sh "terraform plan "
      }
    }
    stage('Terraform Apply') {
      steps {
        input 'Apply Plan'
        sh "terraform apply -auto-approve "
      }
    }
    
  }
}
