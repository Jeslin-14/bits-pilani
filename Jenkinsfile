pipeline {
    agent any

    stages {
        stage('Run Script') {
            steps {
                script {
                    try {
                        sh 'echo "Running script..."'
                        sh 'false' // Simulate a failure
                        // sh 'true' // Simulate success
                    } catch (Exception e) {
                        echo "Script failed!"
                        error "Script failed"
                    }
                }
            }
        }
    }

    post {
        always {
            echo "Pipeline finished."
        }
        success {
            echo "Everything went well!"
        }
        failure {
            echo "Something went wrong!"
        }
    }
}