pipeline {
    agent any
    tools {
        maven 'maven'
    }
    stages {
        stage('src from github') {
            steps {
                git branch: 'master', url: 'https://github.com/Madhan-D249/Development.git'
            }
        }
        stage('build') {
            steps {
                sh 'mvn clean deploy -s Settings.xml'
            }
        }
    }
    post {
        always {
            echo "always"
        }
        success {
            echo "build success"
        }
        failure {
            echo "build failed"
            script {
                currentBuild.result = 'FAILURE'
                error("Deployment failed. Check Nexus server availability and settings.")
            }
        }
    }
}
