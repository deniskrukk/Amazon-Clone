#!groovy
//  groovy Jenkinsfile
pipeline  {
    agent any;
    stages {
        
         stage("Backup files")
         {
             steps{
                sh """
                #!/bin/bash
                sudo /home/azureuser/backup.sh
                """
             }
         }
         stage("Change IP in axios.js")
         {
             steps{
                sh "find FrontEnd/my-app/ -type f -exec sed  -i 's#http://localhost:5034#https://10.20.34.175/api#g' {} +"
             }
         }
    }
}
