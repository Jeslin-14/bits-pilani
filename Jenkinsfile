pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                script {
                    if (env.BRANCH_NAME == 'feature-branch') {
                        git credentialsId: 'Jeslin-14', url: 'https://github.com/Jeslin-14/bits-pilani.git', branch: env.BRANCH_NAME
                    } else {
                        git credentialsId: 'Jeslin-14', url: 'https://github.com/Jeslin-14/bits-pilani.git', branch: 'main' //Or master
                    }
                }
            }
        }
        stage('Build') {
            steps {
                sh 'echo "Building..."'
                // Add your build steps here
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Testing..."'
                // Add your test steps here
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