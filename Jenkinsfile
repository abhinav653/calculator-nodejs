node {
    stage('Build') {
        steps {
            sh 'npm install'
        }
    }

    stage('Test') {
        steps {
            sh 'npm test'
        }
    }

    stage('Containerization') {
        steps {
            script {
                docker.build("abhinav653/calculator-app:1.0")
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}

