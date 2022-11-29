pipeline{
        agent any
        tools {
              terraform 'terraform'
            }
        stages{
            stage("git-checkout"){
                steps{
                git branch: 'main', credentialsId: 'git-credential', url: 'https://github.com/sneha2105/terraform-project'
                }
            }
            stage("terraform init"){
                steps{
                sh 'terraform init'
                }
            }
            stage("terraform apply"){
                steps{
                sh 'terraform apply --auto-approve'
                }
            }
        }
    }
