pipeline {
    agent { label 'Linux' }
    options {
        skipDefaultCheckout true
    }
    tools {
        maven 'maven'
    }
    stages {
        stage ('SCM') {
            steps {
               echo "---------SCM Start----------"
               git branch: 'temp', credentialsId: 'ayaz-github-creds', url: 'https://github.com/azdn949/maven-app.git'
               sh "ls -l"
               echo "---------SCM End------------"
            }
        }
        stage ('Build') {
            steps {
               echo "---------Build Start----------"
               sh "mvn clean install -DskipTests"
               echo "---------Build End------------"
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
    // post { 
    //         cleanup { 
    //             echo "Clean up in post workspace"
    //             cleanWs()
    //         } // End of cleanup
    // }
} // End of Pipeline  