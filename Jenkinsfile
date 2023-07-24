pipeline {
    agent any
    options {
        skipDefaultCheckout true
    }
    stages {
        stage ('SCM') {
            steps {
               //echo "SCM"
               git branch: 'temp', credentialsId: 'ayaz-github-creds', url: 'https://github.com/azdn949/maven-app.git'
            }
        }
        stage ('Build') {
            steps {
               echo "Build"
            }
        }
        stage ('Sonar Scan') {
            steps {
                echo "Sonar Scan" 
            }
        }
        stage ('Push Artifacts to Jfrog Artifactory') {
            steps {
                echo "Push Artifacts to Jfrog Artifactory" 
            }
        }
        stage ('Upload Docker Image to Jfrog Artifactory') {
            steps {
                echo "Upload Docker Image to Jfrog Artifactory" 
            }
        }
        stage ('Deployment') {
            steps {
                echo "Deployment" 
            }
        }
    } // End of Stages
} // End of Pipeline  