pipeline {
    agent any
    tools {
    maven 'MAVEN'
  }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'mvn clean package'
                }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }

}
