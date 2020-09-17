pipeline{
    agent any
    stages{
        stage("Getting code from repo")
        {
            steps{
                
                sh'git clone https://github.com/Pavan-971/Teeraform-Pract.git'
                sh 'pwd'
                
                sh 'terraform init'
                sh 'terraform plan'
                sh 'terraform apply -auto-approve'
                
        
            }
        }
    }
}
