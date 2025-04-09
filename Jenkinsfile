pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                script {
                    if (env.BRANCH_NAME == 'feature-branch') {
                        git credentialsId: 'jeslin_gitId', url: 'https://github.com/Jeslin-14/bits-pilani.git', branch: env.BRANCH_NAME
                    } else {
                        git credentialsId: 'jeslin_gitId', url: 'https://github.com/Jeslin-14/bits-pilani.git', branch: 'main'
                    }
                }
            }
        }
        stage('Build') {
            steps {
                bat 'echo Building...' // Use bat for Windows commands
                // Add your Windows build commands here
            }
        }
        stage('Test') {
            steps {
                bat 'echo Testing...' // Use bat for Windows commands
                // Add your Windows test commands here
            }
        }
    }
    post {
        always {
            echo 'Pipeline finished.'
        }
        success {
            echo 'Build Success'
        }
        failure {
            echo 'Build Failure'
        }
    }
}
//This is the assignment 1 of DevOps