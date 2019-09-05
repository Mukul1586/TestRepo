pipeline {

    agent none 

    stages {
        
      
 stage('Build') {
     
     agent { label 'slave' }

            steps {

                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/Mukul1586/TestRepo.git']]])

            }

        }

        stage('Test') { 
            
             agent { label 'slave' }

            steps {

                bat "echo Test"

            }

        }

        stage('Deploy') { 
            
             agent { label 'slave' }

            steps {

                bat "echo Deploy"

            }

        }

    }

}
