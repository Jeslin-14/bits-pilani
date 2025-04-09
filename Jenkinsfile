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
                bat 'echo Building...'             }
        }
        stage('Test') {
            steps {
                bat 'echo Testing...'             }
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