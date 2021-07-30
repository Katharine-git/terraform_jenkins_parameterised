pipeline{
  
// Environment Variables
env.AWS_ACCESS_KEY_ID = AWS_ACCESS_KEY
env.AWS_SECRET_ACCESS_KEY = AWS_SECRET_KEY

stages{                                                                                 
  stage ('Checkout') {
    git branch: 'master',
       url: 'https://github.com/Katharine-git/terraform_jenkins_parameterised.git'
  }

  stage ('Terraform Plan') {
    sh 'terraform init'
    sh 'terraform plan '
  }

  stage ('Terraform Apply') {
    sh 'terraform apply -auto-approve'
  }
}
}
