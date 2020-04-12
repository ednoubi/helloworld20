pipeline {
    agent any 
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
        stage('test '){
        steps {
          echo "test step"
          sleep 5
        }     
      
        post {
            always {
            echo "Always display this message"
                failure {
                echo "job failed"
                }
                
            }
        }
    }
}
