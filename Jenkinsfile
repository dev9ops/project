pipeline {
    agent any

    stages {
        stage('Terraform Version') {
            steps {
                echo 'Terraform version..'
                sh "/usr/bin/terraform version"
            }
        }
        stage ("plan") {
            steps {
                sh ('terraform plan') 
            }
        }
        stage (" Action") {
            steps {
                echo "Terraform action is --> ${action}"
                sh ('terraform ${action} --auto-approve') 
           }
        }  
}
