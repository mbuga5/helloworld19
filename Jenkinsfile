pipeline {
    agent any
    triggers {
        cron 'H/1 * * * *'
    }
    tools {
        maven 'M2_HOME'
    }
    stages {
      stage('Build'){
        steps {
          echo "Build step"
          sh 'mvn clean'
          sh 'mvn install'
          sh 'mvn package'
        }
      
      
      }
        stage('tests '){
        steps {
          echo "test steps"
          sh 'mvn test'
        }
      
      
      }
        stage('deploy'){
        steps {
          echo "deploy war file"
          build 'peoject16'
        }
      
      
      }
    
    }
    tools {
    danse }
}
