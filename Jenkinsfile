pipeline {

    agent any
    tools {
  maven 'M2_HOME'
}
    triggers {
        pollscm '* * * * *'
    }

    stages {
        stage('maven package') {
            steps {
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
            }
        }
         stage('test') {
            steps {
                echo 'build'
                sleep 5
            }
        }
         stage('test') {
            steps {
                sh 'mvn test'
            }
        }
         stage('deploy') {
            steps {
                echo 'deploy'
        
            }
        }
    }
}
