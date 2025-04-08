pipeline {
    agent any

    stages {
        stage('Run Script') {
            steps {
                script {
                    try {
                        sh 'echo "Running script..."'
                        sh 'true' // Simulate success
                        // sh 'false' // Simulate a failure
                    } catch (Exception e) {
                        echo "Script failed!"
                        //error "Script failed" // Commented out
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